# Action Auditing Overview


Action auditing is a service that provides traceability through logging all user actions performed within IAM in 30 days. For example, create users and login to EnOS.

Each action is recorded as an event.

 A audit log includes the information of the event (what), the actor (who) of the event, the data and time of the occurrence, source IP, whether MFA enabled or not<!--MFA 界面上未看到-->.


## Key functionalities

The audit logs help you check the user actions to achieve the following goals:

- Security analyst:
  Locate and analysis the abnormal actions of the account or resource.

- Troubleshooting:
  Detect the causes of a system error<!--或者是？-->  
  For example, a user cannot access to the authorized service. You can check the related actions to find out the causes.


- Security compliance:
  Audit a user by checking whether this user performed any illegal actions.
