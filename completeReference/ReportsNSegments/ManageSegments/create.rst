Creating Segments
-----------------

To create a new data Segment:

1. Navigate to **Reports & Segments > Manage Segments** in the main menu and click **Create Manage Segments**.

   .. image:: /completeReference/img/ReportsNSegments/ManageSegments/ManageSegmentsCreate.png
      :class: with-border

2. Provide general segment information: 

	.. csv-table::
	  :header: "Field", "Description"
	  :widths: 10, 30

	  "**Name**","Name used to refer to the segment in the system."
	  "**Description**","Segment description aimed to help you and other users understand the purpose or peculiarities of the segment in the future."
	  "**Entity**","Choose an entity from the drop-down. Records of the chosen entity will be selected in the segment."
	  "**Type**","Chose the segment type from the drop-down:
	  
		  - **Dynamic** segments are updated as soon as any changes have taken place in the system 
		  
		  - **Manual** segments will be updated only following the user request  (:ref:`refresh the grid <user-guide-ui-components-grid-action-buttons>` in the View page of the Segment record)"
	  "**Owner**","A business unit, members of which can manage the segment, subject to the `roles <../../System/UserManagement/roles.html>`_ defined in the system."
   
   .. image:: /completeReference/img/common/filters/segments_form.png

3. In the **Columns** section, define the set of fields. Values of the chosen fields will be displayed at the Segment details page. To create add a column to the grid:
  
  * Choose the fields from the drop-down in the *"Column*" section.

  * Choose a label that will be used to refer to the field in the report in UI. 
    The default field label, defined in the field's 
    :ref:`general settings <user-guide-entity-management-general-common>` will be added but can be changed. 
  
  * Define the sorting order if you want the whole segment View grid to be sorted by the field value.

  * Click :guilabel:`Add` button
      
      .. image:: /completeReference/img/common/filters/segments_column.png 

      .. note:: In order to manage the columns, use action icons in the last column:

				  * Delete a column from the segment with |IcDelete|

				  * Edit the column settings with |IcEdit|

				  * Change the column position, dragging the column by the |IcMove| icon

4. In the **Filters** section, define the Activity and/or Data audit and/or Field Condition and/or Condition Group 
filters that will be used to select the records for the segment. See more information about using filters `here <../../../completeRerefernce/commonActions/filter.html>`_. 

5. Click **Save**.


.. |IcEdit| image:: /completeReference/img/common/buttons/IcEdit.png
   :align: middle
   
.. |IcView| image:: /completeReference/img/common/buttons/IcView.png
   :align: middle
   
.. |IcDelete| image:: /completeReference/img/common/buttons/IcDelete.png
   :align: middle

.. |IcMove| image:: /completeReference/img/common/buttons/IcMove.png
   :align: middle