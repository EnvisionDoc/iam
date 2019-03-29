# Creating and Managing Users

This article instructs how to manage ordinary users: internal users within an OU, external users imported from another OU, and LDAP users.

## Creating and Authorizing an Internal User
You can use the following steps create an internal user that natively belongs to an OU.

### Step 1: Creating an Internal User
1. In the EnOS console, click **IAM > User** from the left navigation panel.

2. In the **Internal User** tab, Click **New User**.

3. In the **Basic Information** section, provide the basic information of the new user and click **Next**.

   - **Send By**: You can choose to send the password to the owner of the user account via phone or email. You also can sent the password in other secure offline approaches.

### Step 2: Grant Permission
You can assign permission for a user in the following approaches:
- Granting policies
- Assigning user to the user groups. In this approach, the user will inherit all permissions that are assigned to the user groups.

To grant policies:
  1. In the **Policies** tab, click **Grant Permissions**.

  2. In the pop-up window, select policies to assign to this user and click **Save**.

  3. Click **Save** to create the user.

To add a user to groups:
 1. In the **Add User to Group** tab, click **Add to User Group**.

 2. In the pop-up window, select User group to be assigned to this user and click **Save**.

 2. Click **Save** to create the user.



## Adding and Authorizing an External User

You can add and authorize a user from another OU in the following approaches

### Step 1: Adding an External User

**Adding an user from another OU**

1. In the EnOS console, click **IAM > User** from the left navigation panel.  

2. In the **External User** tab, Click **Import User**.

3. In the pop-up window, enter the full username of the external user. If the name is correct, the detailed information of the user will display in the dialog. Then click **Confirm**.

4. Click **Next**.

**Adding an LDAP User**

To add an LDAP user, you need to first configure the connection to an LDAP server. For more information, see [Getting Started with LDAP Federation](ldap/ldap_gettingstarted).

### Step 2: Grant Permission

Granting permission for a LDAP user is the same as for an internal user.

## Deleting an Internal User

When you delete an internal user, this user account is completely removed from the EnOS Cloud.

1. In the EnOS console, click **IAM > User** from the left navigation panel.  

2. In **Internal User** tab, click |img1| of the user to be deleted.

3. In the pop-up window, click **Confirm** to delete this user account complete.


## Removing an External User
When you remove an external user, this user is removed only from the current organization, the user still exists in its root organization and other organizations that the user is imported into.

1. In the EnOS console, click **IAM > User** from the left navigation panel.  

2. In the **External User** tab, click |img1| of the user to be deleted.

3. In the pop-up window, click **Confirm** to remove this user.

## Resetting Password

1. In the EnOS console, click **IAM > User** from the left navigation panel.  

2. In the **Internal User** tab, click |img2| after the user to reset password for.

3. In the **Edit User Information** page, click **Reset** next to the password. System will generate a new password which shows next to the **Reset**.

4. Store this password in safety and click **Save**.


.. |img1| image:: ../../media/delete.png

.. |img2| image:: ../../media/edit.png

<!--end-->
