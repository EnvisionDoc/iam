# Activity Log Auditing Overview

User activity log auditing allows you to trace the resource access activities of all users that are registered in IAM. For example, the activity that an OU admin created a user at a specific time will be logged into the system for your query. The analysis of activity logs help you trace the dynamics of resource changes and audit for security compliance. In specifics, the activity log auditing help achieve the following objectives:

- **Security analysis**: When security issues occurs on accounts and resources, activity log can help you diagnose the cause of the issues. An _event_ record is created for each user or resource activity. An event record contains comprehensive information such as who accesses which resource at which time and from where. These data helps you identify security risks and violation actions.

- **Resource dynamics tracing**: Trace resource change abnormalities. For example, when an access policy is deleted, which causes all user accounts who are assigned this policy cannot access relevant resources. In this case, you can trace who performed this action through the activity log.

## Key Concepts

- **Event**: An event is an action that a user performs through the EnOS Console or API against a certain _resource_. Each user or resource change activity is logged as an event record.
