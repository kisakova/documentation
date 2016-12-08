Processes System Configuration
------------------------------

To view all Processes, navigate to **System > Processes** in the main menu.

Preview:

.. include:: /completeReference/overview/System/ProcessesOverview.rst
  :start-after: begin


.. image:: /completeReference/img/System/Processes/Processes.png
   :class: with-border

The following information about the Processes is available in the Processes list:

+-----------------+-------------+
| Name            | Description |
+=================+=============+
| NAME            |             |
+-----------------+-------------+
| RELATED ENTITY  |             |
+-----------------+-------------+
| EXECUTION ORDER |             |
+-----------------+-------------+
| ENABLED         |             |
+-----------------+-------------+
| CREATED AT      |             |
+-----------------+-------------+

**Next steps**

You can perform the following actions with every item in the Processes list:

 * Delete

 * View

 * Deactivate


.. rubric:: Managing Processes

.. warning:: Reused from OroCRM. Rework.

Some actions in OroCommerce may trigger the pre-defined additional processes--actions that are executed in the background. In OroCommerce, you can activate or deactivate existing processes.

View Processes
--------------

To view the processes, navigate to the *System → Processes* in the main menu.

The process list contains the following details:

.. csv-table::
  :header: "Name","Description"
  :widths: 10, 30

  "NAME","Defines the process available in the system." 
  "RELATED ENTITY","OroCRM :term:`entity`, records of which are influenced by the process."
  "EXECUTION ORDER","Priority of the process execution. The smaller is the number, the higher is the priority. If 
  several processes have been triggered simultaneously, the processes
  with a higher priority are executed first."
  "ENABLED","If set to *Yes*, the process will be executed."
  "CREATED AT","Date and time when the process was added to the system."

.. image:: /completeReference/img/System/Processes/processes/pr_grid.png

View Process Details
--------------------

Click the |IcView| on the grid to open process details, including the **Process Triggers**, i.e. in what
case and with what delay after the event the process will be executed.

.. image:: /completeReference/img/System/Processes/processes/pr_view.png


Manage Processes
----------------

The only action available from the UI is enabling/disabling the process.

This can be done with :guilabel:`Activate` and :guilabel:`Deactivate` buttons on the View page or |IcDeactivate| and 
|IcActivate| icons on the  *"All Processes"* grid.



.. |IcView| image:: /completeReference/img/common/buttons/IcView.png
   :align: middle
   
.. |IcDeactivate| image:: /completeReference/img/common/buttons/IcDeactivate.png
   :align: middle
   
.. |IcActivate| image:: /completeReference/img/common/buttons/IcActivate.png
   :align: middle