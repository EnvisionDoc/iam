# Setting the Security Options
Current OU owner and administrators can set the password policies, IP address black and white lists, and session expiration time for users to log into the EnOS.

## About This Task

This topic instructs how to configure the security settings for users, including password strength, IP address black and write lists, and session expiration time.

## Before You Start

  You should be organization owner or administrator. However, it is not recommended to use the organization owner account to perform any operations other than transferring the ownership of the organization owner.

## Configuring the Password Policies for This OU

You may implement the requirements on password strength by configuring the password policies.

### Procedure

1. Select **IAM > Security Setting**;

2. Select **Edit**, and you may set proper password policies for OU in the "Password Policy" section.
   
   EnOS supports the following password policies:

   .. csv-table::
      :widths: auto

      "Password Strength", "Requirements"
      "Medium (default)", "- Password length requirements: 8 digits;
      - at least one uppercase English letter
      - at least one lowercase English letter
      - at least one number
      - password expiration (days) enabled: the password remains valid for 180 days (inclusive)
      - Password reuse disabled: the latest 2 passwords are logged for repeat check"
      "Strong", "- Password length requirements: 12 digits;
      - at least one uppercase English letter
      - at least one lowercase English letter
      - at least one number
      - password expiration (days) enabled: the password keeps valid for 90 days (inclusive)
      - Password reuse disabled: the latest 3 passwords are logged for repeat check"
      "Very Strong", "- Password length requirements: 16 digits;
      - at least one uppercase English letter
      - at least one lowercase English letter
      - at least one number
      - at least one special character (including `!@#¥%&*()[]{}-_=|`)
      - password expiration (days) enabled: the password keeps valid for 60 days (inclusive)
      - Password reuse disabled: the latest 5 passwords are logged for repeat check"

3. Click **Save** to complete the configuration of password policies

### Result

The new password policies of this OU should be followed when a new user registering an account; In scenarios where old password policies are replaced by new policies, the following results may occur for the users under the control of the old password policies once the old policies are replaced:

- Password strength upgrade: After stronger policies are saved, EnOS checks password expiration dates for users under the current OU upon the next login; for the users whose passwords would expire in 3 days, an SMS or email will be sent to ask them to modify their passwords according to the new password policies. In this case, the validity period of the new passwords starts from the time when the users reset their passwords 
- Password strength downgrade: After weaker policies are saved, existing passwords would continue to remain valid until they expire. Users can set passwords according to the new password strength when they change their passwords.

.. note:: Do not change the password policies frequently.

## Configuring the Login IP Access Control

You may add specific IP or IP segments to a IP blacklist or whitelist.

### Procedure

1. Select **IAM > Security Setting**, and then click **Edit**
   
2. Select the method to restrict IP addresses in the **Login IP Restrictions**:
   - Whitelist: Only users from the IP address or IP segments on the white list can access the EnOS console; all users are allowed to access the EnOS console by default if the white list is empty
   - Blacklist: Users from the IP address or IP segments on the black list cannot access the EnOS console.
  
3. Enter the IP addresses or IP segments to be controlled. Classless inter-domain routing (CIDR) is supported.

4. Click **Save** to make IP access control take effect immediately.

## Result

- In the whitelist mode, only users from the IP address or IP segments on the white list can access the EnOS console
- In the blacklist mode, users from the IP address or IP segments on the black list cannot access the EnOS console.

## Configuring the session expiration time


### Procedure

1. Select **IAM > Security Setting**, and then click **Edit**
   
2. Set the session expiration time in the **Session Status** field. Valid value ranges from 15 to 1440 minutes.

### Result

When a login request exceeds the expiration time, the session will expire and the user needs to try to log into EnOS again.
