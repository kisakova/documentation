Viewing and filtering all Organizations
---------------------------------------

To view all Organizations, navigate to **System > Organizations** in the main menu.

Preview:

.. include:: /completeReference/overview/System/UserManagement/OrganizationsOverview.rst
  :start-after: begin



.. image:: /completeReference/img/System/UserManagement/Organizations.png
   :class: with-border

The following information about the Organizations is available in the Organizations list:

+---------------+-------------+
| Name          | Description |
+===============+=============+
| NAME          |             |
+---------------+-------------+
| STATUS        |             |
+---------------+-------------+
| CREATED AT    |             |
+---------------+-------------+
| UPDATED AT    |             |
+---------------+-------------+
| GLOBAL ACCESS |             |
+---------------+-------------+

**Next steps**

You can perform the following actions with every item in the Organizations list:

 * View

 * Edit

 * Configuration


You can perform the following actions at the Organizations page:

 * Create Organization


.. RUBRIC:: Managing Organizations

.. warning:: Reused from OroCRM. Rework.

An Organization record represents a real enterprise, business, firm, company or another organization, to which the 
:term:`users <User>` belong. 

.. _user-management-organization-create:

Create an Organization Record
-----------------------------

.. important::

    Creation of new organizations is only available in the Enterprise Edition. 

In order to create an Organization record:

1. Go to *System → User Management → Organizations*.
2. Click the :guilabel:`Create Organization` button.
3. Define the general details and the list of users for the organization created, and specify if it is a 
   :ref:`system organization <user-ee-multi-org-system>`:

The following fields **must** be defined 

.. csv-table::
  :header: "**Name**","**Description**"
  :widths: 10, 30

  "**Status**","Current status of the organization.

  *Inactive* or *Active.*
  "
  "**Name**","The name used to refer to the organization in the UI. This is  the only mandatory field."
 
You can also add a text description of the organization.
 
      |
  
.. image:: /completeReference/img/System/UserManagement/user_management/organization_general.png
 
Users
^^^^^

  Check/uncheck the **HAS ORGANIZATION** box, to assign/unassign a user to the organization.

.. note::

    Please note that the "HAS ORGANIZATION" check-box defines if the user is assigned the organization role that you are
    editing/creating.


Additional
^^^^^^^^^^

In the *"Additional"* section, you can define if the organization is a 
:ref:`system organization <user-ee-multi-org-system>`.


View and Manage an Organization Record
--------------------------------------

In the enterprise edition, all the organizations available are displayed in the Organizations 
grid(*System → User Management → Organizations*).

      |

.. image:: /completeReference/img/System/UserManagement/user_management/organization_action.png

|

From the grid you can:


- Get to the `Edit form <../../../completeReference/Advanced/dataManagement/form.html>`_ of the organization: |IcEdit|.

- Get to the `View page <../../../completeReference/Advanced/data_management/view.html>`_ of the organization: |IcView|.

- Get to the :ref:`configuration settings <admin-configuration>` of the organization: |IcConfig|

In the community edition, you can only edit the organization name and its description. To get to 
the edit page, go to *System → User Management → Organizations*.


.. |IcConfig| image:: /completeReference/img/common/buttons/IcConfig.png
   :align: middle

.. |IcEdit| image:: /completeReference/img/common/buttons/IcEdit.png
   :align: middle

.. |IcView| image:: /completeReference/img/common/buttons/IcView.png
   :align: middle
 