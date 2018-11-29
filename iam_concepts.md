# IAM concepts

This article describes the main concepts of the IAM functional module to help you understand the identity and access management on EnOS.

## Organization

In EnOS, an organization is the top-level management unit, it is a collection of user accounts, assets, and etc. Resources of EnOS Cloud are segregated by organizations. Through IAM, you can centrally manage all users and check user activities within this organization. Each organization has an unique master account called _OU owner_ and multiple other types of user accounts. The OU owner can control the access rights of other users through binding corresponding access policies.

## User Account

 You can create multiple users within one organization. Each user account has its own credential (username and password) to log in to EnOS Console. The authorization of each user is specified by assigning appropriate policies to the user.

The user accounts in EnOS can be divided into the following types:

- **System administrator**
A system administrator is the super user who has complete, unrestricted access to all resources in a cloud instance. Each EnOS cloud instance has one or more system administrators.
  - For public cloud, the sysmtem administrators are the Envision EnOS cloud administrators.
  - For private cloud, the system administrators are usually designated staffs of the client's organization, who are responsible for managing the user accounts and resources at the corporate level.
The system administrator can create OUs and have access to the backend configuration. For more information, see [System management overview](backend/backend_overview).

- **OU owner**
When a new organization unit is created in a cloud instance, a master account called OU owner is generated for the OU. The OU owner has complete, unrestricted access to all resources in this OU, including the access to the IAM module. Therefore, the OU owner can create accounts for other users and authorize the users under this OU via IAM.


- **OU administrator**
The OU owner can create one or more OU administrators. An OU admin is the user who has been assigned the built-in policy _administrator_ which has full access and management privileges, in particular, the access to IAM module. The OU administrators can manage the lifecycle of users and grant access policies for users. For more information, see [Getting started with creating a user account in an OU](iam_gettingstarted_adduser).


- **Ordinary user**
An ordinary user is usually who has the minimum access rights that are just sufficient to complete their job responsibilities on EnOS. The OU owner or OU administrator can create users and assign access policies for the users.

A user account can be added through the following approaches:

  + **Internal user**: An internal user is created natively within a certain organization. The user can be authorized through being added into user groups, or assigned policies directly.

  + **External user**: An external user, in the opposite, is created in other organizations. In EnOS, certain user accounts might need to work across organizations to perform IoT implementation and development. For example, you can import an operation staff, who is created in another organization, into your current organization. Such users can be assigned appropriate access rights in different OUs.

  + **LDAP user**：LDAP users are imported through LDAP federation. For more information, see [LDAP ferdatation](ldap/ldap_overview).

## User Group

A user group is a collection of users. The user group helps you centralize the management of the collection of users who preform the same tasks in EnOS. The policies assigned to a user group are applied to all users that belong to this group.

All types of users ( _Ordinary user_, _external user_, _LDAP user_ ) can be added to a user group.

You can create user groups and define access policies according to business scanarios. For more information, see [Best practice](best_practice).

## Policy

A policy is a collection of permissions to the resources in EnOS (such as services, functions, and data). Policy takes effect only when assigned to a user or user group. You can design policies for different roles according to the user and user group definition based on the granularity that EnOS supports:

- EnOS service and tool: Support menu level authorization.
- Assets data: support access to all assets data.

## Multi-Factor Authentication

 Multi-factor authentication (MFA) adds a layer of protection on top of the password to increase the security of the EnOS cloud. Users need to provide extra factors when they access to EnOS.

 With MFA enabled, when the user attempts to log in to EnOS Console, they need to provide the following factors of credentials:

- Factor 1: the user credential (username and password)
- Factor 2: a verification code received on the registered email or mobile phone.
