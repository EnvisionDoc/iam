# Synchronizing LDAP Users Manually

You can manually synchronize user account data from the LDAP server when the LDAP server is updated. For example, when users or directories have been changed.

## Target Audience
   OU Administrator

## Procedure

1. In the EnOS console, click **IAM > LDAP Federation** from the left navigation panel.  
2. Click **View** of the LDAP connection to be changed.
3. Click **Synchronize** to synchronize the latest user information from the LDAP server.

.. note:: The LDAP users that already exist in EnOS will not be imported again. The LDAP users who are deleted from LDAP server will be deleted from EnOS as well.
