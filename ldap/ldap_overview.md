# LDAP Federation Overview

You can create users from Lightweight Directory Access Protocol (LDAP) federation. EnOS Cloud supports to synchronize users from an LDAP directory to the EnOS user account system and grant permission for these LDAP users.

EnOS allows you to manage LDAP connections, the following facts and rules apply for the LDAP connections in EnOS:

- One organization can connect to one or more LDAP servers. Each LDAP connection can be configured with multiple base DN accounts.  
- Multiple organizations can connect to the same LDAP server.
- Make sure that the user information is consistent between EnOS IAM and the LDAP server. If the user information is changed on the LDAP server, you can manually synchronize the changes to EnOS. And each time when a user logs in, EnOS will detect the account status in the LDAP server.

You can also manage the LDAP users in EnOS just as managing the internal and external users.
- You can group LDAP users and grant permissions for LDAP users. Authorized LDAP users can log in to the EnOS Console with appropriate permissions.
- You can enable and disable the login of LDAP users for an organization.

## Key Concepts

  - LDAP connection: The connection between the LDAP server and EnOS Cloud. An LDAP connection contains the configuration information of the LDAP server.
  - LDAP user: A user who logs in to EnOS via an account that is imported from an LDAP directory.



## LDAP User Login Workflow

The following figure shows the workflow of the EnOS login method.

.. image:: ../media/framework.png

<!--end-->
