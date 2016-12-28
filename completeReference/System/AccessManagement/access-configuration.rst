Access Level Configuration
==========================

.. contents:: :local:
    :depth: 3


Access level defines how much information and how many system capabilities are visible and available your OroCommerce user. Access level may be envisioned as a box. Multiple access levels may be nested. The smaller the box, the more limited set of data a user can access and vice verse. If a user has no box, they have no access whatsoever.
OroCRM has a predefined set of access levels with ``None`` being the most limited and ``Global`` providing the widest access to the data. 

.. image:: /completeReference/img/System/UserManagement/access_roles_management/access_levels2.png 

The complete list of access levels available in OroCommerce are provided below:  

+---------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Access Level  | The data a user can access                                                                                                                                                 |
+===============+============================================================================================================================================================================+
| None          | Access is denied.                                                                                                                                                          |
+---------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| User          | Entity records owned by the user (providing the user has access to the organization(s) for which these records were created).                                              |
+---------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Business Unit | Entity records owned by the business unit(s) the user has access to or by any user that has access to the same business unit.                                              |
+---------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Division      | Entity records:                                                                                                                                                            |
|               | * Owned by business unit(s) the user has access to or by any user that has access to the same business unit.                                                               |
|               | * Owned by the whole chain of the business units subordinated to those the user has access to.                                                                             |
+---------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Organization  | All entity records within the organization the user has access to.                                                                                                         |
|               | **Note**: Organiztion level in not available in OroCommerce Community Edition and may be hidden when there is only one organization in the OroCommerce Enterprise Edition. |
+---------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Global        | All entity records within the system.                                                                                                                                      |
+---------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

.. Important:: 
	An oganization may be marked for global access only. Only users with global access may log into this organization. In this case, other access levels are insufficient and fallback to **None** access level.


Setting Access Levels for a User Role
-------------------------------------

Configure a user role by setting access level for every entity (customer, order, etc.) and every action that can be performed on the entity (view, create, delete, etc.). 

For example, "Account Manager" role has **Global** access to the actions with **Customer**, **Customer Login Page**, **Customer User**, **Customer User Address** and **Customer User Role**, and they do not have access to other actions with other objects (access level is **None**).

To limit customer account manager permissions to activities only withing their organization, create a dedicated role with *Organization* set to customer's organization, or set the **Organization** access level for actions with **Customer**, **Customer Login Page**, **Customer User**, **Customer User Address** and **Customer User Role**.

For more information and examples please see the `Role Management </completeReference/System/UserManagement>`_.

.. important:: Some entities support only **None** and **Global** access level. Ability to set other access levels depends on the entity’s ownership type. You can set an access level that is higher than or equal to the entity’s ownership type. Thus, if an entity's ownership type is **Business Unit**, the **User** access level is disabled for actions on this entity. For more information see the `Ownership type and access levels </completeReference/System/AccessManagement/ownership.html#ownership-types-and-access-levels>`_ section in the `Ownership Type </completeReference/System/AccessManagement/ownership.html>`_.

  
Access Level for Individual Data Fields
---------------------------------------

Generally, the data access is managed on the record level (you can grant permission to create a Customer). Record contains a number of fields - unitary bits of information, e.g. **Name**, **Organization**, **Description**, **Website**, etc. You might want to hide certain fields from one group of users while still having them available for others. 

.. note:: In OroCommerce Field ACL is available only for custom entities.

To enable Field Level ACL for a custom entity:

#. Navigate to the **System > Entities > Entities Management** and click Edit next to the necessary entity from the list. 

#. In **Other** section, enable the **Field Level ACL** by setting the checkbox.

.. image:: /completeReference/img/System/UserManagement/access_roles_management/access_field_level_acl_enable.png

5. Click :guilabel:`Save`.

.. important::
	Currently, Field Level ACL functionality is available only for custom entities.

After the Field Level ACL is enabled, the field permissions appear below the entity permisions in the `role details </completeReference/System/UserManagement/roles.html>`_.

.. image:: /completeReference/img/System/UserManagement/access_roles_management/roles_permissions_fields_general_ex.png 

The list of available actions for entity fields is smaller than for an entity:

+--------+-------------------------------------------------------------------------------+
| Action | Description                                                                   |
+========+===============================================================================+
| View   | A user can see entity record fields in the grid and on the record view pages. |
+--------+-------------------------------------------------------------------------------+
| Create | A user can see and modify entity record fields on the 'new entity' form.      |
+--------+-------------------------------------------------------------------------------+
| Edit   | A user can see and modify entity record fields on the 'edit entity' form.     |
+--------+-------------------------------------------------------------------------------+

For each of these actions you can set an access level, thus defining the range of entity records which fields a user can perform an action on: will the be only the records owned by a user themselves, records of the user's division, all records in the system, etc.

.. Important::
	Note that for entity fields, the set of available access levels depends on:

	- Entity's ownership type. For example, you won't be able to set the **User** access level for a field if the entity's ownership type is **Organization**. 
	- Action. For the **Create** action only the **None** (access is denied) and *Global* (access all entity records within the system) access levels are available independently of the entity's ownership type.

For more information about how access levels are configured for entities please see the `Setting Access Levels for a User Role <Setting Access Levels for a User Role>`_ above.

For more information about ownership types, see the Ownership type and access levels section `here </completeReference/System/AccessManagement/ownership.html>`_.

.. caution:: 
	Ability to assign permissions for entity fields is a powerful tool that gives you an opportunity to tune up user roles in OroCommerce on a granular level. If you restrict a user from viewing a particular field, consider restricting them from editing this field as well to avoid confusion when these fields are visible in the edit mode.


Restricted (Read-Only) Fields
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

To provide read-only access to a subset of information, you can limit access to the particular fields in edit mode to users of the senior role. For users with less permissions these fields will appear dimmed.

.. image:: /completeReference/img/System/UserManagement/access_roles_management/opportunity_greyed-status.png 


To enable viewing the restricted fields:

#. Navigate to the **System > Entities > Entities Management** and click Edit next to the necessary entity from the list. 

#. Click **Others**.

4. In the **Other** section enable the **Show Restricted** by setting a check box.

|

.. image:: /completeReference/img/System/UserManagement/access_roles_management/access_field_level_acl_showrestricted.png

|

5. Click :guilabel:`Save`.

Related Information
^^^^^^^^^^^^^^^^^^^

* `User Management </completeReference/System/UserManagement>`_.
* `Access Configuration: Examples </completeReference/System/AccessManagement/example.html>`_.
