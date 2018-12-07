# FAQ's

The topic lists frequently asked questions about IAM.

## Q: What kind of user account can configure LDAP federation?
   A: LDAP Federation is a service module in IAM which is only visible to OU owner or OU administrator. Therefore, only the OU owner and OU administrator allow to enable, disable and configure LDAP federation.


## Q: If the LDAP authentication is disabled, can users imported from the LDAP server still login?
   A: No. The LDAP user cannot login when LDAP authentication is disabled.


## Q: If the LDAP connection is deleted, can users imported from this LDAP server still login?
   A: No. When deleting a LDAP connection, the users imported from this LDAP server is removed from the EnOS as well.


## Q: Can users imported from LDAP being added to other organization as an external user?
   A: No, you can't. The LDAP user cannot be added as an external user to other organizations. Only the users that natively created in EnOS can be import to other organizations as an external user.

## Q: What is the retention period for EnOS Audit logs?
   A: EnOS Audit stores logs for 30 days.


## Q: What kind of events will be logged into audit log?
   A: Currently, Audit only recorded the event happens in IAM. For detailed event list, see [Event Log Schema](../audit/log_details.)
