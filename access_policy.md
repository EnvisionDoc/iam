# Policies, Roles and Permissions

A policy is a collection of permissions to the resources in EnOS (such as services, functions, and data). You can assign the access policies to a user, a user group or an application to manage the resources that are accessible for them in EnOS. A policy takes effect only when assigned to a user, user group, or application. You can assign different policies as needed for a user or a user group based on the granularity that EnOS supports.

- EnOS service and tool: support menu-level authorization.
- Assets and data: support access to all assets within an OU.

The access policies in IAM are classified into two types: _built-in policies_and_custom policies_.


## Built-in policies

The built-in policies, which cannot be edited or deleted, refer to a collection of the access policies that are pre-defined for typical user roles in the EnOS. For example, any user that is assigned with "Model Administrator" owns the write and read permissions to create, delete, edit, import, export, view and instantiate the models under the OU.

The following built-in policies are available in EnOS:

.. csv-table::
   :widths: auto

   "Role", "Permissions"
   "Administrator", "Owns the permissions to access and manage all the resources in the OU"
   "Security Auditor", "Owns the permissions to view all the security settings and audit logs in the OU"
   "Model Administrator", "Owns the write and read permissions to create, delete, edit, import, export, view and instantiate the models in the OU, including system admin, industry experts responsible for model management, O&M personnel responsible for model deployment"
   "Model User", "Owns the read-only permission to view, export and instantiate the models in the OU, including average users and implementation personnel"
   "Asset Tree Administrator", "Owns the write and read permissions to create, delete, edit and view the asset trees in the OU,  including system admin, asset admin and asset implementation personnel"
   "Asset Tree User", "Owns the read-only permission to view the asset trees in the OU, including average users and application developers"
   "Connectivity Provisioning Administrator", "Owns the write and read permissions to create, delete, edit and view the connectivity configurations in the OU,  including system admin, asset admin and asset implementation personnel"
   "Connectivity Provisioning User", "Owns the read-only permission to view the connectivity configurations in the OU, including average users and application developers"

## Custom policies

The custom policies refer to the access polices customized as per the needs of users and service accounts to access EnOS services. For example, a user that only needs to query the models may be assigned with the "read-only" permission to "Model Management Services".

EnOS now supports the custom access permissions to the following services:

.. csv-table::
   :widths: auto

   "Service", "Resources", "Permission"
   "Connectivity Provisioning Management", "Connectivity configurations", "- Full Access,
   - Read Only"
   "Asset Tree Management (Console)", "Asset trees in the EnOS console", "- Full Access,
   - Read Only"
   "Model Management", "Models", "- Full Access,
   - Read Only"
   "Asset Tree Data Services (Device Data)", "Data of the devices under an asset tree", "- Control,
   - Edit"

Note:
- Full Access: write and read permissions to create, delete, edit and view the objects.
- Read Only: read-only permissions to only view the objects.

  Permissions to asset tree data include the following:
  - Read: read-only access to assets.
  - Control: permission to send commands to assets.
  - Write: permission to edit device attributes.
