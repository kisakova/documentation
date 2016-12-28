Viewing and filtering all Business Units
----------------------------------------

To view all Business Units, navigate to **System > Business Units** in the main menu.

Preview:

.. include:: /completeReference/overview/System/UserManagement/BusinessUnitsOverview.rst
  :start-after: begin



.. image:: /completeReference/img/System/UserManagement/BusinessUnits.png
   :class: with-border

The following information about the Business Units is available in the Business Units list:

+------------+-------------+
| Name       | Description |
+============+=============+
| NAME       |             |
+------------+-------------+
| EMAIL      |             |
+------------+-------------+
| PHONE      |             |
+------------+-------------+
| OWNER      |             |
+------------+-------------+
| CREATED AT |             |
+------------+-------------+

**Next steps**

You can perform the following actions with every item in the Business Units list:

 * View

 * Edit

 * Delete


You can perform the following actions at the Business Units page:

 * Create Business Unit

.. rubric:: Managing Business Units

.. warning:: Reused from OroCRM. Rework.

Create a Business Unit Record
-----------------------------

In order to create a :term:`Business Unit` record:

- Go to *System → User Management → Business Units*
- Click the :guilabel:`Create Business Unit` button
- Define the general details of the business unit created:

General
^^^^^^^

.. csv-table::
  :header: "**Name**","**Description**"
  :widths: 10, 30

  "**Name**","The name used to refer to the business unit in the UI. This is the only mandatory field."
  "**Parent Business Unit**","Define the business unit to which this business unit belongs (a level higher in the 
  administrative hierarchy), if applicable."
  "**Phone**
  
  **Website**
  
  **Email**
  
  **Fax**","You can define these contact details of the business unit, if applicable."
  

.. image:: /completeReference/img/System/UserManagement/user_management/bu_general.png  
  
Users
^^^^^
  Check/uncheck the **HAS BUSINESS UNIT** box to assign/unassign a user to the business unit:

.. note::

    Please note that the "HAS BUSINESS UNIT" check-box defines if the user is assigned the specific business unit that 
    you are creating/editing

View and Manage a Business Unit Record
--------------------------------------

All the business units available are displayed in the Business Units 
grid(*System → User Management → Business Units*).

From the grid you can:


- Delete a business unit from the system: |IcDelete|

- Get to the `Edit form <../../../completeReference/Advanced/dataManagement/form.html>`_ of the business unit: |IcEdit|

- Get to the `View page <../../../completeReference/Advanced/data_management/view.html>`_ of the business unit: |IcView|




.. |IcDelete| image:: /completeReference/img/common/buttons/IcDelete.png
   :align: middle

.. |IcEdit| image:: /completeReference/img/common/buttons/IcEdit.png
   :align: middle

.. |IcView| image:: /completeReference/img/common/buttons/IcView.png
   :align: middle
 
