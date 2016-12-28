Creating Roles
==============

To create a role, the seller will need to navigate to the customer tab located in the top menu and click on “Account User Roles.” In the image below, we’ve already created three different roles: Administrator, Buyer, and Role1. To begin the process of creating a new role, simply click on the blue button labelled “Create a New Role.” The form will then take the user through the necessary steps in a logical way.

Once the seller has entered in the name of the role and the accounts this role belongs to, he will go through the steps of assigning the action permissions and access levels for each entity (e.g., account, account user, account address, etc.) by clicking on the blue “None” link and allowing/disallowing access. Obviously, this entity list can be modified and other actions can be added or deleted using configuration files. In a similar way, the seller can assign capabilities and then assign account users to this role. (Note: This only works if account users were already created. If not, the seller should save the record and go back to it after the account users have been entered into the system).

.. image:: /completeReference/img/System/UserManagement/Roles/Role.png
   :class: with-border


Borrowed from updated CRM
=========================

Actions with Roles
===================

.. contents:: :local:
    :depth: 3


Actions
--------

Create a Role
^^^^^^^^^^^^^^

1. In the main menu, navigate **System>User Management>Roles**.
    
2. Click the :guilabel:`Create Role` button in the upper-right corner of the page. The **Create Role** page opens.

3. Click **General**, and in the **Role** field, type the role name. Note that the name must be unique for the system.

.. image:: /completeReference/img/System/UserManagement/access_roles_management/role_create1.png


4. Click **Additional** and specify the following:

   - **Description**—Type the description of this role. Use the in-built text editor to format the provided description.
   
   - **Organization**—Select the organization for user's of which this role will be applicable. If you want this role to be applicable for all organizations defined in the system, do not specify any organization. In this case the field value becomes **System-wide.** (If there is only a single organization defined in the system or you do not have global access rights, there will be no option for selecting an organization.)
	
|

.. image:: /completeReference/img/System/UserManagement/access_roles_management/role_create2.png

|

5. Click **Entities**. In this section define which 'action on entity' permissions and which capabilities you want to include in the role. For more information about the 'action on entity' permissions and capabilities, see the `Roles Management <./access-management-roles>`__ guide.
 
   1. For each action on each entity specify the required access level. By default, for all entities access levels are set to **None**. Choose an entity which you want to assign different permissions for. In the entity row, click the action name and in the drop-down list, click the required access level. For more information about the access levels, see the `Access Levels <./access-management-access-levels>`__ guide.
   
   |
   
   .. image:: /completeReference/img/System/UserManagement/access_roles_management/role_create_entities_acl2.png

   |

   If you want to set the same access level for all actions on entity, you can complete it in one move: from the ellipsis menu at the right-hand end of the entity row, select the required access level.

   |

   .. image:: /completeReference/img/System/UserManagement/access_roles_management/roles_create_entities_acl1.png

   |

   If you want to set individual permissions for the entity fields, please see the `Include Permissions for an Entity Field in a Role  <./access-management-roles-actions#include-permissions-for-an-entity-field-in-a-role>`__ section for how to do this. 
   
   2. Under the list of entities, select the check boxes in front of the required capabilities.  
   
   |

   .. image:: /completeReference/img/System/UserManagement/access_roles_management/role_create_entities_acl2.png

   |
   
6. Click **Users**, and in the grid, select check boxes in front if the users to whom you want to assign this role.

|
   
.. image:: /completeReference/img/System/UserManagement/access_roles_management/role_create_entities_acl2.png

|

7. lick the :guilabel:`Save` button in the upper-right corner. 