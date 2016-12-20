Display Settings
----------------

In *"System → Configuration → General setup → Display settings"* you can define a number of display-related options
to be applied to the OroCRM instance, as follows:

      |
  
.. image:: /completeReference/img/System/Configuration/configuration/display_settings.png

Navigation bar
^^^^^^^^^^^^^^

In the **Navigation bar → Position*** field, define the *Navigation bar* position. Choose a value from the drop-down
menu.

The default value is "Top".

WYSIWYG settings
^^^^^^^^^^^^^^^^

In the  **WYSIWYG settings → Enable WYSIWYG Editor*** field, define whether text formatting tools must be available for 
:ref:`emails <user-guide-activities-emails>`, :ref:`notes <user-guide-add-note>` and 
:ref:`comments <user-guide-activities-comments>`. 

The value is enabled by default.

.. note::

    The formatting tools can also be enabled for other text fields in the course of integration.


Activity lists
^^^^^^^^^^^^^^

The activity list setting define different options to be applied to display activities (created calendar events, sent emails, loged calls, attachments, comments, notes, assigned tasks)
in the UI.

The following options are available:

.. csv-table::
  :header: "Option", "Description", "Default"
  :widths: 10, 30, 10

  "**Sort By Field*** and **Sort Direction***","Defines the field and direction used to sort activities in the grid by 
  default (every time you open a page with the grid.) You can changed the sorting of the grid each time.","By default 
  the activities updated last will be shown at the top."
  "**Items Per Page By Default***","Defines the number of activities displayed on one page of the grid by 
  default (every time you open the grid.) You can changed the number each time.","10"

Data Grid settings
^^^^^^^^^^^^^^^^^^

Data Grid settings define different options used to display all the 
:ref:`entity records grids <user-guide-ui-components-grids>` in the UI.

The following options are available:
 
.. csv-table::
  :header: "Option", "Description", "Default"
  :widths: 10, 30, 10

  "**Items Per Page By Default***","Defines the number of items displayed on one page of the grid by 
  default (every time you open the grid.) You can change the number each time.","25"
  "**Lock Headers In Grids***","Defines whether grid headers will be locked on a page during scrolling.","Enabled"
  "**Record Pagination***","If enabled, you can navigate to previous or next item in the system when viewing item details,"Enabled"
  "**Record Pagination Limit***","Defines a maximum number of records available for the *Record Pagination*. (If there 
  are more records, the pagination will be disable for the grid to avoid performance deterioration) ","1000"

Calendar settings
^^^^^^^^^^^^^^^^^^  

Calendar settings specify the colors available to manage calendars in the UI:

.. csv-table::
  :header: "Option", "Description", "Default"
  :widths: 10, 30, 10
  
  "**Calendar Colors***","A set of colors available for different users' calendars.

  |CalCol1|","|CalCol1Def|"
  "**Event Colors***","A set of colors available for different events in the user's calendar.

  |CalCol2|","|CalCol2Def|"
  

Sidebar settings
^^^^^^^^^^^^^^^^

With the Sidebar settings you can enable or disable the left and/or right sidebar to keep your Sticky notes and Task lists. 
By default only the right sidebar is enabled.

Reports Settings
^^^^^^^^^^^^^^^^

If this function is enabled, users can see the SQL request sent to the system for a report.

|

.. image:: /completeReference/img/System/UserManagement/Roles/sql_show.png

|

This way, users can check if a report has been developed correctly.

.. hint::

    This link will only be available if the :ref:`View SQL query of a report/segment <admin-capabilities-view-sql>` 
    capability has been enabled for the role.


.. |CalCol1| image:: /completeReference/img/System/Configuration/configuration/cal_col_1.png
   :align: middle
   :scale: 50%
   
.. |CalCol1Def| image:: /completeReference/img/System/Configuration/configuration/cal_col_1_def.png
   :align: middle
   

.. |CalCol2| image:: /completeReference/img/System/Configuration/configuration/cal_col_1.png
   :align: middle
   :scale: 50%
   
.. |CalCol2Def| image:: /completeReference/img/System/Configuration/configuration/cal_col_1_def.png
   :align: middle