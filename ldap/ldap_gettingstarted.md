# Getting started with LDAP federation

This topic instructs how to import the LDAP users from LDAP server and authorize LDAP user in IAM.

Workflow of getting started with LDAP users
![Image](media/flow1.png)
(TBD)


## Target audience
   System Administrator


## Before you begin

   1. Ensure that the LDAP users have been created in the LDAP service and the LDAP server is working properly.
   2. Known the username and password of administrator account of the LDAP server. This administrator account should at least have full access permissions to all the base DNs.
   3. An user with LDAP administration authorization has been created. For detailed information, see [Managing User](../managing_user.md).
   4. The access policy for LDAP federated users have been created in EnOS IAM. For detailed information, see [Managing policy](../managing_policies.md).

## Procedure

### Step 1： Establish LDAP server connection

   To establish the LDAP server connection:

   1. Log on to EnOS cloud with an user has LDAP administrator authorization.
   2. In the navigation panel, click **IAM>LDAP Federation** .
   3. In **LDAP** page, Click **New LDAP Federation**. And configure the LDAP connection as below.

      - **Realm**: The unique identity of the LDAP connection.
      - **Primary LDAP server**: The URL or IP address of the LDAP server.
      - **Port number**：Optional, port number of the LDAP server.
      - **base DN**: The root distinguished name (DN) to use when importing users against the directory server. Support configure multiple base DNs under one LDAP server at once. Multiple base DNs are separated by semicolon (;). For example: cn=users,dc=example,dc=com;ou=users,dc=example,dc=com.
      - **Filter**: You can define a condition filter to limit the entries within base DNs.For example: FILTER=memberOf=CN=group,CN=developers,DC=example,DC=com.
          **Note**: Ensure that the entries have been selected are all valid account entries.
      - **User DN or name**: User name of the LDAP administrator account.
      - **Password**: Password of the LDAP administrator account.
      - **Attribute mapping**: Define the mapping relationship between system attributes and LDAP attributes.

![Image](media/newldap.png)   (TBD)

   3.   Click **Test**. It checks the connection to LDAP server, legality of the information and data obtaining.

       - If pass the test, click **Done** to create the LDAP connection.
       - If doesn't pass the test, you need to check the information you enter is correct and re-test.


## Step 2：Enable LDAP Authentication

   After the LDAP connection has been created, in **LDAP Connection** page, click the **LDAP Authentication** to enable LDAP users login.




## (Optional) Step 3: Import LDAP users to EnOS IAM

Import the LDAP users in advance can help you to authorize your LDAP users in batch.

    - The authorized LDAP users can directly log on to EnOS Cloud with appropriate permissions.
    - Otherwise, the unauthorized LDAP users cannot access to any services after first login. LDAP user needs to contact system administrator to grant permissions.

   1. In **LDAP Federation**, click the **View** after the LDAP server to be edit.

   2. Click **Import account**, then the LDAP users have been selected is imported to EnOS IAM.
      **Note**: The LDAP users that already exist in the IAM is not imported again.



## Step 4: Authorize LDAP users

   You can authorize the LDAP user individually or by adding to a authorized group. For more information, see [Managing user](../managing_users.md)


## Results
The LDAP users that have been imported and authorized can login to EnOS Cloud with appropriate permissions.
