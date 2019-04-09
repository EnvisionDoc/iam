# Enabling the Multi-factor Authentication

Multi-factor authentication (MFA) adds a layer of protection on top of the password to increase the security of EnOS. Users need to provide extra factors when they access to EnOS.

With MFA enabled, when users attempts to log in to the EnOS console, they need to provide the following credentials:

- Factor 1: the user credential (user name and password)
- Factor 2: a verification code received on the registered email or mobile phone.

This topic introduces how to enable multi-factor authentication for an OU.

## About This Task

This topic describes how to enable multi-factor authentication for users within an OU.

## Before You Start

- You are the organization owner or have the OU admin account.

## Procedure

1. Select **IAM > User**.

2. In the **User** page, toggling the **MFA** switch to enable or disable the multi-factor authentication.
   
   If you want to configure MFA at OU level, enable or disable the multi-factor authentication for all users within the current organization.

## Result

Once MFA is enabled, EnOS will provide proper authentication options based on the registration information (e.g. email address, phone number) provided by the user for authentication:

- If a user provides only the phone number, additional SMS-based verification would be performed for logging in;
- If a user only provides the email address, additional email verification would be performed for logging in;
- If both the email address and the phone number are provided by the user, the SMS-based verification would be performed for logging in by default; however, the user may choose email-based verification.
