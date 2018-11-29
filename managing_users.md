# Creating and managing users

This article instructs how to manage ordinary users: internal users within an OU, external users imported from another OU, and LDAP users.

## Creating and authorizing an internal user
You can use the following steps create an internal user that natively belongs to an OU.

### Step 1: Creating an internal user
1. In the EnOS console, click **IAM > User** from the left navigation panel.  
2. In the **Internal User** tab, Click **New User**.
3. In the **Basic Information** section, fill in the basic information of the new user and click **Next**.
   - **Send By**: You can choose to send the password to the owner of the user account via phone or email. You also can sent the password in other secure offline approaches.

### Step 2: Grant permission
You can assign permission for a user in the following approaches:
- Granting policies
- Assigning user to user groups. In this approach, the user will inherit all permissions that are assigned to the user groups.

To grant policies:
  1. In the **Policies** tab, click **Grant Permissions**.
  2. In the pop-up window, select policies to assign to this user and click **Save**.
  3. Click **Save** to create the user.

To add user to groups:
 1. In the **Add User to Group** tab, click **Add to User Group**.
 2. In the pop-up window, select User group to be assigned to this user and click **Save**.
 2. Click **Save** to create the user.

<!--可能会被移到gettingstarted里-->


## Adding and authorizing an external user

How to add and authorize a user from another OU.

### Step 1: Import an external user
1. In the navigation panel, click **IAM > User**.
2. In the **External User** tab, Click **Import User**.
3. In the pop-up windows, enter the full username of the external user. If the name is correct, the detailed information of the user will display in the dialog. Then click **Confirm**.
4. Click **Next**.

## Adding and authorizing an LDAP user

To add an LDAP user, you need to first configure the connection to an LDAP server. For more information, see [Getting started with LDAP federation](ldap/ldap_gettingstarted).

### Step 2: Grant permission

Granting permission for an external user is the same as for an internal user.

## Deleting an internal user

When you delete an internal user, this user account is completely removed from the EnOS Cloud.

1. In the navigation panel, click **IAM > User**.
2. In **Internal User** tab, click ![Image](media/delete_icon.png) after the user to delete.
3. In the pop-up window, click **Confirm** to delete this user account complete.


## Remove an external user
When you remove an external user, this user is removed only from the current organization, the user still exists in its root organization and other organizations that the user is imported into.

1. In the navigation panel, click **IAM > User**.
2. In the **External User** tab, click ![Image](media/delete_icon.png) after the user to delete.
3. In the pop-up window, click **Confirm** to remove this user.

## Resetting password

1. In the navigation panel, click **IAM > User**.
2. In the **Internal User** tab, click ![Image](media/edit_icon.png) after the user to reset password for.
3. In the **Edit User Information** page, click **Reset** next to the password. System will generate a new password which shows next to the  **Reset**.
4. Store this password in safety and click **Save**.
