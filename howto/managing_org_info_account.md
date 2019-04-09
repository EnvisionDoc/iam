# Managing the Organization Information and Organization Accounts

An organization is the top-level account management unit, and it is a collection of users, resources, applications and services. An organization is responsible for paying for the resources it owns, and fully controls these resources.

## About This Task

This article describes how to manage and maintain the organization information and change the organization owner.

## Before You Start

You should prepare an account with proper permissions for the operations to be performed:
- If you want to edit the organization information, an organization owner account or an administrator account is required.
- If you want to change the organization owner, an organization owner account is required.

## Editing the Organization Profile

You may edit the organization profile to change the details of your organization, such as name, address, business license No., industry, country, and scale of your organization.

### Procedure

1. Select **IAM > Organization Profile**;


2. Click **Edit** to edit the basic information, and then click **Save** after modification.
   You can modify the following fields:
   - Organization name
   - Organization ID
   - Address
   - Business license No.
   - Industry
   - Country
   - Scale
   
   In these fields, the **Organization name** field is mandatory.

3. Modify the information as needed, then click **Save**.

### Result

Click **IAM > Organization Profile**, and you will see the updated basic organization information.

## Changing the Organization Owner

### Procedure

1. Select **IAM > Organization Profile**;


2. Select **Change** under the Organization Owner;


3. In the user name drop-down menu, select the target user; if this user have not registered any email address, manually enter the user email address and click **Confirm**, and then a confirmation email will be sent to the email address of this user;


4. The target user can click the given link in this confirmation email to confirm, and then the organization owner will be transferred to the new user;


   .. note:: The link in the email remains valid for 24 hours by default. You can cancel the operation to change owner if the target user fails to confirm the ownership transfer within this period.


   

### Results

The following results may occur after the target user clicks the given link in the confirmation email:
- The ownership transfer would be successful if the link remains valid and the original owner of the OU does not cancel the ownership transfer;
- The link would be invalid and the ownership transfer would fail if the link does not remain valid, or the original owner cancels the transfer operation or the link has been clicked;
- The link would become invalid and the transfer operation would fail if any other exception occurs.

Once the transfer operation completes, the original owner will become an average user with all originally-granted permissions revoked; if the user has logged in, a prompt indicating expired login will pop up for the next user action, and the user will not have any permissions once logged in again.  

The target user becomes the new organization owner. This transfer of ownership takes effect upon next login or user action.


