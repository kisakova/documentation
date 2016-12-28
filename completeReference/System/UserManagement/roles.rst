Viewing and filtering all Roles
-------------------------------

To view all Roles, navigate to **System > Roles** in the main menu.

Preview:

.. include:: /completeReference/overview/System/UserManagement/RolesOverview.rst
  :start-after: begin

.. toctree::
   :maxdepth: 1

   Roles/index

.. image:: /completeReference/img/System/UserManagement/Roles.png
   :class: with-border

The following information about the Roles is available in the Roles list:

+-------+-------------+
| Name  | Description |
+=======+=============+
| LABEL |             |
+-------+-------------+

**Next steps**

You can perform the following actions with every item in the Roles list:

 * Clone

 * View

 * Edit

 * Delete


You can perform the following actions at the Roles page:

 * Create Role


:rubric: Managing Access and Permissions

.. warning:: Reused from OroCRM. Rework.

.. _user-guide-user-management-permissions-ownership-type:

Ownership Types
---------------

Each entity in OroCRM has an :ref:`ownership type <user-guide-entity-management-create-other>` type, which defines the 
level at which permissions will be set for records of the entity.

If the ownership type is set to *"None"*, no authorization is required to see and process the entity and all the users
within the OroCRM instance will be able to view, create, edit, delete and assign records of the entity. Otherwise, they
depend on the specific Role settings, as described below. 

.. _user-guide-user-management-permissions-roles:

Roles
-----
Each OroCRM :term:`user <User>` must be assigned a role. The role defines a set of permissions and access rights that 
will be applied to all the users who have been assigned this role.
One user may have several roles. All the permissions granted to at least one of the roles assigned to a user, 
are granted to the user. 

If the ownership type of an entity is set to a *"User"*, *"Business Unit"* or *"Organization"*, the ability to see and 
process the entity records is defined by the role(s) assigned to the user.

Roles and Permissions
^^^^^^^^^^^^^^^^^^^^^
For each entity with an ownership type other than *"None"*, you can define permissions to perform the following actions: 

- View: If, for a specific entity, the action is not available to a user, the user won't see the records 
  grid nor the `View pages <../../../completeReference/Advanced/data_management/view.html>`_ 
  of this entity records.
  
- Create: If, for a specific entity, the action is not available to a user, the user won't be able to create new entity 
  records.

- Edit: If, for a specific entity, the action is not available to a user, the user won't be able to edit the entity 
  records.

- Delete: If, for a specific entity, the action is not available to a user, the user won't be able to delete the
  entity records.
  
- Assign: If, for a specific entity, the action is not available to a user, the user won't be able to change the owner 
  of the entity records.

.. image:: /completeReference/img/System/UserManagement/user_management/role_entity_dropdown.png

For each entity and action you can define one of the permission settings, depending on the entity ownership type and
whether it is a system organization with global access, as described below:


Permissions for System Organizations
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

In a system organization, the user will able to perform an action for the
entity records in any organization within the system, as long as the permission is set to *"System"*.

      |
  
.. image:: /completeReference/img/System/UserManagement/Organization/multi_org/multi_org_permission.png

|
  
Any other permission setting but *"System"*, in a system organization, will be treated as *"None"*.


Permissions for Non-System Organizations
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Permissions in non-system organizations depend on the ownership type of the entity.

      |

Ownership Type: Organization
~~~~~~~~~~~~~~~~~~~~~~~~~~~~

If the entity type is set to *"Organization"*, when an entity record is created, an :term:`organization <Organization>` 
is chosen as its :term:`owner <Owner>`. 

You can choose one of the following options for each action: 

- **None**: No users will be able to perform the action.
- **Organization**: All the users from the owner-organization will be able to perform the action.
- **System**: All the users will be able to perform the action.

  |

Ownership Type: Business Unit
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

If the entity type is set to "Business Unit", when an entity record is created, a :term:`business unit <Business Unit>` 
is chosen as its Owner. 

You can choose one of the following options for each action: 

- **None**:  No users will be able to perform the action.
- **Business Unit**: All the users from the owner-business-unit will be able to perform the action.
- **Division**: All the users from the owner-business-unit and from its child business units will be able to perform 
  the action.
- **Organization**: All the users from the organization to which the owner-business-unit belongs, will be able to 
  perform the action.
- **System**: All the users will be able to perform the action.

  |

Ownership Type: User
~~~~~~~~~~~~~~~~~~~~

If the entity type is set to "User", when an entity record is created, a :term:`user <User>` is chosen as its owner. 
You can choose one of the following options for each action: 

- **None**: No users will be able to perform the action.
- **User**: Only the owner-user will be able to perform the action.
- **Business Unit**: All the users from the business unit to which the owner-user belongs will be able to perform the 
  action.
- **Division**: all the users from the business unit to which the owner-user belongs and from its child business units 
  will be able to perform the action.
- **Organization**: all the users from the organization, to which the owner-user belongs, will be able to perform the 
  action.
- **System**: all the users will be able to perform the action.

Roles and Access Rights
^^^^^^^^^^^^^^^^^^^^^^^
Access right assigned to a role, define if the users will be able to access a specific functionality.
There are only two options:

- **None**: users with the role won't be able to use the functionality.
- ***System***: users with the role will be able to use the functionality for all the records created within their
  OroCRM instance they've logged in into.

Creating a Role
---------------

To create a new role:

- Go to *System → User Management → Roles*.
- Click the :guilabel:`Create Role` button.

  |
  
  |role_create|

  |
  
- In the form that has emerged, define the role name that will be used to assign it to a user.

  Define other settings in the sections described below:
  
  - **Entity**: Define what permissions the users assigned this role will have for the entity records that have 
    an ownership type other than "None".
  - **Capabilities**: Define if the user that has been assigned this role will have access to certain parts of the 
    system.
  - **Users**: Select users to be assigned this role.

The "Entity" Section
^^^^^^^^^^^^^^^^^^^^

If the ownership type of an entity is set to "None", it will appear in the *Entity* section of the *"Create Role"* form.
Choose the permissions for each section from the drop-down menu:

      |
  
.. image:: /completeReference/img/System/UserManagement/user_management/role_entity.png

.. hint::
    
    The *"Default"* field specifies the permission settings that are by default assigned to a new entity.


The "Capabilities" Section
^^^^^^^^^^^^^^^^^^^^^^^^^^

The "Capabilities" section contains a list of system functionalities that can be either enabled or disabled for all the 
users that have been assigned a specific role.

      |
  
.. image:: /completeReference/img/System/UserManagement/user_management/role_capabilities.png
  
The "Users" Section
^^^^^^^^^^^^^^^^^^^

In the "Users" section, you can choose users to be assigned the role created.

Check/uncheck the **HAS ROLE** box to assign/unassign a user to the role:

      |
	  
.. image:: /completeReference/img/System/UserManagement/user_management/role_users.png

.. note::

    Please note that the "HAS ROLE" check-box defines if the user is assigned the specific role that you are 
    editing/creating.


Manage Roles
------------

Once a role has been created, it will be added to the "All Roles" 
grid(*System → User Management → Roles*).

From the grid you can:


- Delete the role from the system: |IcDelete|. If there is at least one user that has this role, the role cannot be 
  deleted.

- Get to the `Edit form <../../../completeReference/Advanced/dataManagement/form.html>`_ of the campaign: |IcEdit|. 



.. |IcDelete| image:: /completeReference/img/common/buttons/IcDelete.png
   :align: middle

.. |IcEdit| image:: /completeReference/img/common/buttons/IcEdit.png
   :align: middle


.. |role_create| image:: /completeReference/img/System/UserManagement/user_management/role_create.png
   :align: middle



:rubric: Borrowed from  updated CRM

Roles Management
----------------

.. warning:: Reused from OroCRM. Rework.


.. contents:: :local:
    :depth: 3

Overview
^^^^^^^^

Roles are predefined sets of permissions. When you assign a role to a user, you can be sure that the user will be able to access only that information within the system which is necessary for them to do their work. 

Roles Creation
^^^^^^^^^^^^^^

Usually roles are created based on the user's job functions: sales manager, marketing team member, administrator. But this is not a strict rule. You can create as many roles as required and configure them according to the needs of your company. 
For how to create a role, see the `Create a Role <./access-management-roles-actions#create-a-role>`__ section of the the `Actions with Roles <./access-management-roles-actions>`__ guide. 



Role Structure
^^^^^^^^^^^^^^

A role is a set of permissions that you can grant to a user all-in-one. 
There are two nominal types of permissions in OroCRM: 

- Permissions to perform a certain action on entity. For each permission of this type you can specify a desired access level.

- Permissions to access system functionalities. They are also called 'capabilities' on the interface. System functionalities belong to the system and thus for them you simply specify whether to include permissions to access them into the role or not. 



.. image:: /completeReference/img/System/UserManagement/access_roles_management/user_access.png 


Action on Entity Permissions
~~~~~~~~~~~~~~~~~~~~~~~~~~~~

On each entity in the system a user can perform a certain set of actions. The set may vary for some entities but in general it looks as follows:

+-----------+----------------------------------------------------------------------------+
| Action    | Description                                                                |
+===========+============================================================================+
| View      | A user can see the entity records in the grid and open their view pages.   |
+-----------+----------------------------------------------------------------------------+
| Create    | A user can create a new entity record.                                     |
+-----------+----------------------------------------------------------------------------+
| Edit      | A user can edit entity records.                                            |
+-----------+----------------------------------------------------------------------------+
| Delete    | A user can delete an entity record.                                        |
+-----------+----------------------------------------------------------------------------+
| Assign    | A user can change the owner of an entity record.                           |
+-----------+----------------------------------------------------------------------------+
| Share     | A user can share an entity record with other users.                        |
|           | This action is available only in OroCRM EE.                                |
+-----------+----------------------------------------------------------------------------+
| Configure | A user can set up the system configuration for themselves and other users. |
|           | This action is available on for the **User** entity.                       |
+-----------+----------------------------------------------------------------------------+

For each of this actions you can set an access level, thus defining the range of entity records a user can perform an action on: will these be only the records owned by the user themselves, records of the user's division, all records in the system, etc.?  


The picture below shows the scheme of how permissions for an entity may be configured:

|

.. image:: /completeReference/img/System/UserManagement/access_roles_management/ex_permissions-on-entity.png 

|

This is how the corresponding configuration looks on the interface for the **Account** entity:

|

.. image:: /completeReference/img/System/UserManagement/access_roles_management/roles_permissions_general_ex.png 

|


For more information about which access levels defines which range, see the `Access Levels <./access-management-access-levels>`__ guide.

.. Important::
  Note that the set of available access levels depends on the entity's ownership type. For example, you will not be able to set the **User** access level if the entity's ownership type is **Organization.** Only two access levels are always available: **None**—access is denied and **Global**—access all entity records within the system.
  For more information about ownership types, see the `Ownership Type <./access-management-ownership-type>`__ section and specifically, the `Ownership type and access levels <./access-management-ownership-type#ownership-types-and-access-levels>`__ subsection.

System Functionalities Permissions
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Permissions of this type either define whether a user must have access to certain parts of the system (e.g., should they see the page with system jobs queue) or extend 'action on entity' permissions (e.g. should a user retain the ability to modify their own user profile if editing of user profiles in general is forbidden for them). Permissions of this type are also called 'capabilities.'' Capabilities can be either enabled or disabled for a role. 

This is how capabilities look on the interface:


|

.. image:: /completeReference/img/System/UserManagement/access_roles_management/roles_overview2.png 

|


Assign and Combine Roles
^^^^^^^^^^^^^^^^^^^^^^^^

Each OroCRM user must be assigned a role. A user can have several roles. This is a logical approach if we assume that roles may be based on job functions. For example, if you have roles 'Leads Development Representative' and 'Sales Representative' and some employees do both of these jobs, you simply assign them both roles instead of creating a specialized role that will cover the whole range of required permissions. 
For how to assign a role to a user, see the `Assign Roles While Creating a New User <access_roles_management#assign-roles-while-creating-a-new-user>`__ section. 


If a user has two or more roles with different permissions, in the result the user will have the maximum of rights granted by all of them.   

The following example shows what access level for an action on entity a user who is assigned two roles with different permissions will have:

+------------------------+----------------------------+----------------------------+
| Role 1                 | Role 2                     | Role 1 + Role 2            |
+========================+============================+============================+
| Entity: Account        | Entity: Account            | Entity: Account            |
|                        |                            |                            |  
| Action: View           | Action: View               | Action: View               |
|                        |                            |                            | 
| Access Level: **User** | Access Level: **Division** | Access Level: **Division** |
+------------------------+----------------------------+----------------------------+


Field Level ACLs
^^^^^^^^^^^^^^^^

All important information that comprises an entity is contained in the entity fields. For example, if you open any record of the **Business Unit** entity, you will see such fields as **Name**, **Organization**, **Description**, **Website**, etc. 

When you include the permission to view entity records in a role, users with such role are automatically able to see all fields of the entity. 

However, there are situations when it is desirable to hide certain fields from one group of users while still having them available for others. For example, both the sales team and support team require to see **Opportunity** entity records. But as the financial information is often considered sensitive, you may want to hide the **Budget Amount** field from the support team members.  


Is is possible to do this using Field Level ACL functionality. When you enable it for an entity, you can assign permissions that allow actions on a particular entity field to a role. 

For more information about the field level ACLs, see the `Permissions for an Entity Field (Field Level ACLs) <./access-management-field-level-acl>`__ guide.


Links
-----

For how role is represented on the interface, see the `Roles on the Interface <./access-management-roles-inteface>`__ guide.

For what actions you can perform with roles, see the `Actions with Roles <./access-management-roles-actions>`__ guide.

For examples on roles application, see the `Access Configuration Examples <./access-management-examples>`__ guide.


.. |IcRemove| image:: /completeReference/img/common/buttons/IcRemove.png
  :align: middle

.. |IcClone| image:: /completeReference/img/common/buttons/IcClone.png
  :align: middle
