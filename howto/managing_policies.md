# Creating and Managing Policy

This article instructs how to manage policies that define the access permissions to specific resources. This task is the prerequisite to managing the custom access rights of user, user groups, and service accounts.

## Creating a Policy

You can create a policy in the following approaches:

- Granting permission to certain services
- Granting full permission to all the services including newly added service.

1. In the EnOS console, click **IAM > Policy** from the left navigation panel.   

2. Click **New Policy**.

3. In the **Basic Information** page, provide the basic information of the policy. Then click **Next**.

4. In the **Grant Permissions** page, you can define permissions to the services by ticking the checkbox of the services to be granted.

5. Click **Save** to complete creating the policy.


## Deleting a Policy

When you delete a policy, EnOS revokes corresponding permissions for users, user groups, or service accounts who have been granted this policy.

1. In the EnOS console, click **IAM > User policy** from the left navigation panel.

2. Click the delete icon |delete| for the policy to delete.

3. In the pop-up window, click **Confirm** to complete deleting this policy.

.. |delete| image:: ../media/delete.png

<!--end-->
