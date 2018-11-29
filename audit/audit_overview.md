# Action Auditing Overview

Action auditing is a service that provides traceability through logging all user actions performed within IAM. For example, OU admin creates a user at 10 o'clock will be logged in to the system.

EnOS records these actions as the event logs.

The event log helps you check the events to achieve the following goals:

- Security analyst:
  Locate and analysis the abnormal actions of an account or a resources.

- Troubleshooting:
  Detect the reason of the system errors.
  For example, a user cannot access to the authorized service. You can check the related actions to find out the causes.

- Security compliance:
  Audit a user by checking whether this user performed any illegal actions.

## Key concepts

- Event log: Each action is recorded by EnOS into the  event log. The event log includes the information of the event (what), the actor (who) of the event, the data and time of the occurrence, source IP, whether MFA is enabled or not and etc.

- Resource: Resources is a term to call the policy, the user and the user group.
