# Managing Service Accounts

The service account is a special EnOS account, which is required when an application accesses the resources on EnOS through APIs. Authorizing a service account allows applications to access the authorized resources on EnOS.

## About This Task

This topic describes how to authorize the service account for applications.

## Before You Start

- You must be an OU administrator.

- You have registered an application on the current OU, or have purchased an application from another OU. For more information, refer to [Managing Applications](https://www.envisioniot.com/docs/app-development/en/latest/managing_apps.html).

## Procedure

1. Select **IAM > Service Account**;

2. Select the application to be authorized on the list, then click **Authorize** to enter the Authorization page;
   If the application is not registered, click **Application Registration**, and then return to the Service Account page to continue the authorization.

3. Click the **Assign Policies** button, select the policy to be added for this service account in the pop-up window, then click **+** to grant the permissions to the application, and click  **Save**;
   The list of selectable permissions includes built-in permissions by default and the custom permissions.

4. On the Authorization page, click **Save** to complete the authorization operations.

## Result

On the Service Account page, click **Authorize** to enter the list of policies, and you may check whether the current application is authorized successfully, and the permissions granted successfully will be displayed in the list.
