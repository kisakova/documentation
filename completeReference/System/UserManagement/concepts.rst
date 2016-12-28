User Management Concepts
^^^^^^^^^^^^^^^^^^^^^^^^


Administrative Structure
~~~~~~~~~~~~~~~~~~~~~~~~

The elementary unit of the administrative structure is a **user**. This is a person, group of people or a third 
party system with a specific set of credentials (login and password). 

Any amount of users can be created within one OroCommerce system. 

Users can be grouped into **business units**. 

Any amount of users can be assigned to a business unit. One user can 
belong to several business units simultaneously.

Every business unit may be a parent for one or more children-business-units. A parent business unit and its sub-units are jointly addressed as a **division**.


The most general element of the structure is an **organization**. It represents a real enterprise, business, firm, company,
or another organization, to which the users belongs. 

.. note::

    In the OroCommerce Community edition only organization is supported.

    In the OroCommerce Enterprise edition, several organizations can be created within one system.

User Groups
~~~~~~~~~~~

You can also assign a user to a User Group. User groups may be created in consideration of an administrative structure 
or regardless of it (e.g., all the users born in February or all the users invited to a specific meeting). A 
user group may be used in the system as a single aggregating entity.

By default, user groups are used in the `notification rules <../Emails/notification-rules.html>`_ and 
`filters <../../commonActions/filter.html>`_.

The ways to create and manage the groups is described in the 
`User Group Management <groups.html>`_ section.

User Roles
~~~~~~~~~~

User Roles define access rights of a specific user, as described in the 
:ref:`Access and Permissions Management guide <user-guide-user-management-permissions-roles>`.

Getting Started
~~~~~~~~~~~~~~~

You always have at least one organization and one user who can create other users and who may be authorized 
to create business units and (in the enterprise editions) new organizations. 

When creating/editing the records, you can define their basic details and the following relations.

**For each organization:**

- Users that belong to the organization (in the Enterprise edition only)

The ways to create and manage the organization records is described in the `Organization Management guide <organizations>`_


**For each business unit:**

- Users that belong to the business unit
- Parent unit of the business unit

The ways to create and manage the business unit records is described in the 
`Business Unit Management <business-units.html>`_ section.

**For each user:**

- Organizations the user belongs to
- Business units the user belongs to
- Groups the user belongs to
- Role assigned to the user

The ways to create and manage the user records is described in the 
`User Management <users>`_ section.

