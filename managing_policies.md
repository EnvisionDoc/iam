# Creating and managing policy

This article instructs how to manage policies that define the access permissions to specific resources.

## Creating a policy

You can create a policy in the following approaches:

- Granting permission to certain services
- Granting full permission to all the services including newly added service.

1. In the EnOS console, click **IAM > User policy** from the left navigation panel.   
2. Click **New Policy**.
3. In the **Basic Information** page, fill in the basic information of the policy. Then click **Next**.
4. In the **Grant Permissions** page, you can define permissions to the services by ticking the checkbox of the services to be granted.
5. Click **Save** to complete creating the policy.


## Deleting a policy

 When you delete a policy, users and user groups who have been granted this policy, EnOS will revoke corresponding permissions for the affected users.

1. In the EnOS console, click **IAM > User policy** from the left navigation panel.   
2. Click the delete icon ![image](media/delete_icon.png) for the policy to delete.
3. In the pop-up window, click **Confirm** to complete deleting this policy.
