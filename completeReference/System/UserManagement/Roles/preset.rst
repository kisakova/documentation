Preset Capabilities by Role
---------------------------

.. warning:: Reused from OroCommerce. Rework.

.. contents:: :local:

:rubric: Administrator

Capabilities List
^^^^^^^^^^^^^^^^^

The *"Capabilities"*  are an important part of the system's access and permission settings, as described in the 
`Access and Permissions Basics <../../../Advanced/dataManagement/access-permissions-basics.html>`_ section. 

Users have access to different functionalities depending on which capabilities they have been assigned. For example, you 
can limit a user's ability to assign tags, share grids, or create new users.

For each role and capability pair, there are only two options:

- **None**: users with this role won’t be able to use the relevant functionality.
- ***System***: users with this role will be able to use the relevant functionality for all the records created within 
  the OroCommerce instance they’ve logged into.
  
.. image:: /completeReference/img/System/UserManagement/Roles/roles/01.png   
  
This guide describes, in alphabetical order, the set of capabilities that are available and their related 
functionalities, and provides examples of several default capability settings for some common roles.

Data Audit
----------

If this capability is set to *"System,"*  the user can see the full history of changes made to any record of an
auditable entity, as well as an out-of-the-box report of all such actions. 

The report is available from the "*System*" menu and described in more details in the 
`Data Audit <../../../Advanced/dataManagement/data-audit.html>`_ section.

The link to a specific record's history of changes is available in the top right corner of the record’s details page.

|

.. image:: /completeReference/img/Advanced/data_management/view/view_history.png

|

This Data Audit is usually used by system administrators, but may also be used by managers in order to see how details 
of different records were changed, as well as by whom.

Export Entities
---------------

If this capability is set to *"System,"* the user can export an entity's records into a .CSV file, as 
described in the `Import and Export Data <../../../commonActions/import.html>`_ section. 

The :guilabel:`Export` button will appear in the top right corner of the page.

|

.. image:: /completeReference/img/System/UserManagement/Roles/roles/export.png 

|

Export is a general productivity tool that is usually enabled for most users.

General Import/Action Operations
--------------------------------

his capability enables common operations for import and export, such as the ability to load the error log. It is 
recommended that you set this capability to *"System"* if either *"Export Entities"* or *"Import Entities"* is also 
set to *"System."* 

Import Entities
---------------

If this capability is set to *"System,"* the user can import records from a .CSV file to OroCommerce, as described 
in the `Import and Export Data <../../../commonActions/import.html>`_ section. The :guilabel:`Import` button will 
appear in the top right corner of the page.

|

.. image:: /completeReference/img/System/UserManagement/Roles/roles/import.png 

|

This is necessary for users who need to import large sets of data into the system. For example, these may include sales 
representatives or employees responsible for lead development.

Jobs Management
---------------

If this capability is set to *"System,"* users can see jobs that have been started in the system, as well as view their 
current status and their performance log from the *"Job Queue*" and *"Sheduled tasks"* pages. Links to these pages are 
available in the *"System"* menu.

The *"Job Queue*" and *"Sheduled tasks"* pages are usually used by system administrators.

Manage Configurable Entities
----------------------------

Many entities in OroCommerce can be configured from the UI, as described in the
`Entities <../../Entities/entity.html>`_ section. The user can change the attachments settings, 
define whether the entity should be displayed on a Grid and/or a View page, whether it will be 
exported to a .CSV file, and define other settings. For some of them, it is also possible to add new fields, as 
described in the :ref:`Entity Fields guide <user-guide-field-management>`. 

These actions are only available if the *"Manage Configurable Entities"* capability is set to *"System."* 

They are usually performed by the system administrators.

Manage Organization Calendar Events
-----------------------------------

If this capability has been set to *"System,"* users can create, edit, and delete events in organization-wide calendars, 
which are described in more detail in thee :ref:`corresponding section <user-guide-calendars-system>` of the 
*Calendars Overview* guide.

Organization calendar events are usually managed by organization-level managers and HRs.

.. hint::

     Even if this capability is set to *"None,"* users can still view organization-wide calendars, add 
     them to their own calendar views, and copy related events to their own calendars.

Manage System Calendar Events
-----------------------------

If this capability has been set to *"System,"* users can create, edit, and delete events in system-wide calendars, which 
are described in more detail in the <user-guide-calendars-system>` of the *Calendars Overview* guide.

System calendar events are usually managed by the company managers and HRs.

.. hint::

     Even if this capability is set to *"None,"* users can still view organization-wide calendars, add them to their 
     own calendar views, and copy related events to their own calendars.

Manage System Calendars
-----------------------

If this capability has been set to *"System,"* users can 
:ref:`create <user-guide-calendars-system>` and :ref:`manage <user-guide-calendars-manage>` system-wide calendars.

System-wide calendars are usually created and managed by system administrators and top managers.

Manage Users' Passwords
-----------------------

If the capability is set to *"System"*, the user can change the passwords of other users. Usually, this is only done
by system administrators when creating or editing a user record. 

.. hint::

    This capability does not influence a user's ability to edit their own 
    password from the *"My User"* page.

Merge Entities
--------------

If the capability is set to *"System,"* users can :ref:`merge <user-guide-ui-components-grids-delete-merge>` 
several records of the same entity.

By default, this capability should be set to *"System."*

Read Address Dictionaries
-------------------------

If the capability is set to *"System,"* the user can access countries, regions, and address types via the API.
It has to be set to *"System"*  in order to support Lead creation via Outlook. This capability should be activated for
system administrators or integrators who are authorized to access OroCommerce via the API.

Search
------

If the capability is set to *"System,"* the user can use the :ref:`search <user-guide-getting-started-search>` 
functionality to quickly find specific records.

This is a general capability that can improve the overall experience of all users.

The setting does not influence the user's ability to :ref:`search by tag <user-guide-getting-started-search-tag>`.

Share Grid View
---------------

If this capability is set to *"System,"* the user can share the grid views 
that they have configured. This way, they can :ref:`adjust a grid <user-guide-ui-components-grids-adjust>` and share it 
with other users.

This is particularly useful for team-leads and heads of departments who want to modify and share grids with their 
subordinates.

|

.. image:: /completeReference/img/System/UserManagement/Roles/roles/grid_share.png

|


System Information
------------------

If this capability is set to *"System,"* the user can view the system information page. This page contains the list of 
Oro packages and third-party packages that are installed, and is usually only used by system administrators and 
integrators.

System Configuration
--------------------

If this capability is set to *"System"*, the user can access the system configuration page 
to localize the system, change the display and tracking settings, and otherwise change the system configuration.


Tag Assign/Unassign
-------------------

If this capability is set to *"System"*, the user can  assign/unassign tags which are 
non-hierarchical keywords or phrases assigned to records. They provide additional information about records and
are visible to all the system users. 

Tags can be successfully utilized by all users.


Unassign All Tags From Entities
-------------------------------

This capability is only meaningful if *"Tag assign/unassign"* is set to *"System."*

If the both *"Tag assign/unassign"* and *"Unassign All Tags From Entities"* capabilities are set to *"System,"* 
users can unassign not only the tags that they have added, but any tags other users have also added to records.

This way, you can restrict users from deleting tags made by other users. This is usually available to 
team leads, department heads, and managers.


Unshare Grid View
-----------------

If this capability is set to *"System,"* users can unshare grids previously shared by themselves. This is usually available to all users who work 
with grids.


View SQL Query of a Report/Segment
----------------------------------

If this capability is set to *"System,"* users see the SQL request that is sent to the system for a report/segment.

Usually, this is only granted to system administrators so they can check if a report has been developed correctly.  
The *"Show SQL Query"* link will appear below the report.

|

.. image:: /completeReference/img/System/UserManagement/Roles/roles/sql_show.png

|


This setting will only work if it has been enabled within *"System Configuration --> Display Settings --> 
Report settings.*" 

|

.. image:: /completeReference/img/System/UserManagement/Roles/roles/sql_setting.png

|


Workflow Manipulations
----------------------

If this capability is set to *"System,"* users can manage the records, that are associated with workflows. Otherwise, users may be able to see and edit records, but will 
not be able to change the status of the records within the workflow.

This capability may be set to *"None"*  in order to restrict users from changing the status of records.


Default Configurations Table
----------------------------

In this table, you will find several default configurations that have been created for different user roles. By default, 
system administrators have access to all capabilities, while other roles are limited by their functions, as shown below.

.. csv-table::
  :header: "", "Admin", "Marketing Representative", "Sales Manager", "Sales Representative"
  :widths: 35, 10, 10, 10, 10

  "**Capability**","System","None","System","None"
  "**Abandoned Cart Campaign manipulations**","System","None","System","None"
  "**Data audit**","System","None","System","None"
  "**Dotmailer Statistic**","System","None","System","None"
  "**Export entities**","System","System","System","None"
  "**General import/action operations**","System","None","System","None"
  "**Import entities**","System","System", "System","None"
  "**Jobs management**","System","None","None","None"
  "**MailChimp manipulations**","System","None","System","None"
  "**Manage configurable entities**","System","None","System","None"
  "**Manage organization calendar events**","System","None", "System","None"
  "**Manage system calendar events**","System","None","System","None"
  "**Manage system calendars**","System","None","System","None"
  "**Manage users' passwords**","System","None","System","None"
  "**Merge entities**","System","None","System","None"
  "**Outlook integration**","System","System","System","System"
  "**Read address dictionaries**","System","None","System","System"
  "**Search**","System","System","System","None"
  "**Send campaign emails**","System","None","System","None"
  "**Share grid view**","System","None","System","None"
  "**System Information**","System","None","None","None"
  "**System configuration**","System","None","None","None"
  "**Tag assign/unassign**","System","None","System","None"
  "**Unassign all tags from entities**","System","None","System","None"
  "**Unshare grid view**","System","None","System","None"
  "**View SQL query of a report/segment**","System", "None","None","None"
  "**Workflow manipulations**","System","System","System","System"