Viewing and filtering all Workflows
-----------------------------------

To view all Workflows, navigate to **System > Workflows** in the main menu.

Preview:

.. include:: /completeReference/overview/System/WorkflowsOverview.rst
  :start-after: begin


.. image:: /completeReference/img/System/Workflows/Workflows.png
   :class: with-border

The following information about the Workflows is available in the Workflows list:

+-------------------------+-------------+
| Name                    | Description |
+=========================+=============+
| NAME                    |             |
+-------------------------+-------------+
| RELATED ENTITY          |             |
+-------------------------+-------------+
| ACTIVE                  |             |
+-------------------------+-------------+
| SYSTEM                  |             |
+-------------------------+-------------+
| PRIORITY                |             |
+-------------------------+-------------+
| EXCLUSIVE ACTIVE GROUPS |             |
+-------------------------+-------------+
| EXCLUSIVE RECORD GROUPS |             |
+-------------------------+-------------+
| CREATED AT              |             |
+-------------------------+-------------+

**Next steps**

You can perform the following actions with every item in the Workflows list:

 * Clone

 * View

 * Deactivate


You can perform the following actions at the Workflows page:

 * Create Workflow




Create a Workflow
^^^^^^^^^^^^^^^^^

.. hint:: 

    Prior to creating a workflow in the system, it is a good idea to draw the sequence of steps and transitions.

In order to create a workflow for an entity:

1. Go to the *System → Workflows* page and click the :guilabel:`Create Workflow` button in the top right corner to get
   to the *Create Workflow* page.
   
   |create_wf_page|

2. Define `general workflow details <General Workflow Details>`_.

3. Define possible `workflow steps <Workflow Steps>`_.

4. Define `transitions <Workflow Transitions>`_ that can be applied to the records at each of 
   the steps and related setting, including the `attributes <Transition Attributes>`_ that 
   can/must be changed after the transition. 
   
5. Choose a `default step <Default Step>`_ if any.

6. Click the button in the top right corner to save the workflow.

.. note::
   
    A transition can be defined as soon as there is at least one step except the "Start". However, it is often 
    simpler to define all the steps and then all the transitions between them.

  
General Workflow Details
~~~~~~~~~~~~~~~~~~~~~~~~

Define basic information in the *General* section.

.. image:: /completeReference/img/System/Workflows/workflows/wf_general.png

The following two fields are mandatory and **must** be defined:

.. csv-table::
  :header: "**Field**","**Description**"
  :widths: 10, 30

  "**Name**","Name used to refer to the workflow in the system."
  "**Related Entity**", "A drop-down to choose an entity, for which the workflow is created."
  
**Display Steps Ordered** box is not checked by default and specifies the way workflow steps are displayed on the 
`workflow widget <user-guide-worfklow-widget>`. 

- When the box is not checked, only the step that have actually been performed are shown and the current step is 
  highlighted.

.. image:: /completeReference/img/System/Workflows/workflows/wf_display_widget.png
  
- When this box is checked, all the possible workflow steps are shown and the current step is highlighted

.. image:: /completeReference/img/System/Workflows/workflows/wf_display_widget_ordered.png

.. note::

   The functionality can be a bit confusing for branching workflows (so, in the example, you can see both Disqualified 
   and Opportunity steps), but is rather useful for linear workflows, as the user can see possible future steps.

Workflow Steps
~~~~~~~~~~~~~~

Define possible workflow steps in the *Designer* section.

1. The first `Start step <user-guide-worfklow-start-step>` is already defined. You need it as a start point for the 
   first transition.

2. To add a step, click the :guilabel:`+ Add Step` button

  |wf_designer_step|

3. Define necessary step details in the "Add New Step" form.

.. image:: /completeReference/img/System/Workflows/workflows/wf_designer_step_form.png

.. csv-table::
  :header: "**Field**","**Description**"
  :widths: 10, 30

  "**Name**","Name used to refer to the step in the system.
  
  Name is the only mandatory field of a step"
  "**Position**", "A number that defines a place where the step will be displayed on the  
  :ref:`workflow widget <user-guide-worfklow-widget>`.
  
  .. note::
  
    Position may be specified with any non-negative integer.

    The step position on the widget depends on the order only (e.g. 0,2,70). 

    Steps with the same position are displayed in the order they have been performed. If a step with a smaller 
    position value has been performed later, steps with higher position values are not displayed in the widget."
  "**Final**","The flag shall be checked for final steps of the flow"

Workflow Transitions
~~~~~~~~~~~~~~~~~~~~

Define possible transitions in the *Designer* section.

1. The first "Start" step is already defined. You need it a start point for the first transition.

2. To add a step, click the :guilabel:`+ Add Transition` button

  |wf_designer_transition|

3. Define necessary step details in the "Add New Transition" form.

.. image:: /completeReference/img/System/Workflows/workflows/wf_designer_transition_form.png

The following fields are mandatory:

.. csv-table::
  :header: "**Field**","**Description**"
  :widths: 10, 30

  "**Name**","Name used to refer to the transition in the system."
  "**From step** and **To step**", "A dropdown that contains the list of steps defined for the workflow. You can choose any 
  two steps and define the transition between them."
  "**View form**","When a transition is performed, a form with the entity 
  :ref:`attributes <user-guide-workflow-designer-attributes>` appears that will be submitted to change the step.
  Use the field, to define if this form will be displayed in a popup window or a separate page."
  
There is also a number of optional fields that can be used to modify the transition in the UI:

.. csv-table::
  :header: "**Field**","**Description**"
  :widths: 10, 30

  "**Warning Message**","A piece of text that will be displayed every time a user is about to perform the transition."
  "**Button icon**","Icon used when displaying the transition button"
  "**Button Style**","Choose the transition button style from the dropdown."

In the **Button preview** you can see how the button will look in the UI.

Transitions Attributes
~~~~~~~~~~~~~~~~~~~~~~

In order to define the attribute settings:

- Go to the *Add Transition → Attributes* 

  |wf_designer_transition_attributes|
  
.. csv-table::
  :header: "**Field**","**Description**"
  :widths: 10, 30

  "**Entity Field**","Choose attributes of the entity or of its related entities that can/must be defined in the course 
  of the transition.
  
  This is an only mandatory field of the attributes section"
  "**Label**","Use the field if you want to change the way it is displayed in the UI. The system *label* value of the 
  entity is used by default."
  "**Required**","The flag shall be checked if defining the attribute must be mandatory for the transition."
 
- Click :guilabel:`+ Add` button to add one more field (if necessary)

- Click :guilabel:`+ Apply` to apply the attribute settings.


Default Step
~~~~~~~~~~~~

You can also define a default step for the records of the entity, processed by the workflow. 

If a default step is specified, once you create a record of the entity, a workflow will be created for it and set to the
default step. 

If no default step is specified, one of the transitions from the "Start" step must be performed to create a workflow for the
record. 

UI Limitations for Workflow Creation
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
 
OroCRM workflows can be created from both the back-end and the UI. However, there is a number of functions that can be 
defined for a workflow only from the back-end in the course of integration:
 
 
- Define Init and Post Actions such as creation of another entity, processing of the existing entity data, 
  email notifications, and other similar actions performed right before of after the transition.

 
- Define precondition and conditions to check if the transition can be performed.
  If preconditions are not met, the transition button is not available, and the transition cannot be submitted. 
  Conditions play a similar role but influence only the ability to submit a transition. 
 
- Define validation for the data entered during the transition.

- Create attributes for records not related to the entity.

This way, Workflows created from the UI are comparatively simple and aimed at processing of the records already present
in the system.

.. note::

    This only means that more complex workflows that require the features shall be defined in the course of 
    integration. This effects your ability to use them in the UI.

Workflows Visualization
~~~~~~~~~~~~~~~~~~~~~~~

All the workflows, whether they were created from the back-end or in the UI, can be applied to the records of a related
entity.

If an initial action that creates a new record of the entity has been defined (from the back-end) for the workflow,
the transition buttons are available in the top right corner of the entity `grid <../../completeReference/Advanced/dataManagement/grid.html>`.

E.g. :guilabel:`Start From Lead` and :guilabel:`Start From Opportunity` that create a new Lead or Opportunity record
at the start of a Sales Process.


.. image:: /completeReference/img/System/Workflows/workflows/wf_display_grid.png


Button of all the transitions, for which pre-conditions (if any) are met, are displayed at
`View pages <../../completeReference/Advanced/data_management/view.html>`_ of the entity records.

E.g. :guilabel:`Develop`, :guilabel:`Close As Won` and :guilabel:`Close As Lost` buttons on a View page of a Sales 
Process record qualified to an opportunity.


.. image:: /completeReference/img/System/Workflows/workflows/wf_display_view.png

.. _user-guide-worfklow-widget:


The current step, or all the steps performed can be displayed on the entity grid, subject to the *Entity Management → 
Workflow Step on Grid* settings.

.. image:: /completeReference/img/System/Workflows/workflows/wf_display_step.png


All the performed steps of the workflow are displayed at the **widget** on the top of the View pages of the entity records, 
subject to the *Workflows → General → Show Ordered* and *Workflows → Designer → POSITION* settings.

.. image:: /completeReference/img/System/Workflows/workflows/wf_display_widget.png


Managing Workflows
^^^^^^^^^^^^^^^^^^

System Workflows
~~~~~~~~~~~~~~~~

System workflows are pre-implemented in the system and are of high importance for proper system functioning, thus their
management from the UI is limited. 

The following actions can be performed for the system workflows:

From the :ref:`grid <user-guide-ui-components-grids>`

.. image:: /completeReference/img/System/Workflows/workflows/wf_grid_actions_system.png

- Activate or deactivate the workflow: |IcActivate| or |IcDeactivate|

.. caution::
    
    Each entity may have an unlimited number of workflows related to it, but only one of them can be active. 

    When a new workflow is activated for an entity, all the workflow data for the entity is reset.

- Clone the workflow: |IcClone|. A copy of the workflow is created and can be customized.

- Get to the `View page <../../completeReference/Advanced/data_management/view.html>`_ of the channel:  |IcView|

From the `View page <../../completeReference/Advanced/data_management/view.html>`_:

.. image:: /completeReference/img/System/Workflows/workflows/wf_view_system.png

You can deactivate, activate and clone the workflow with corresponding action buttons in the top right of the page. 


Custom Workflows
~~~~~~~~~~~~~~~~

Copies of the system workflows and workflows created in the UI from the scratch are custom workflows. 

All the actions available for the system workflows are available for the custom ones.

The following additional action are available for the custom workflows:

From the :ref:`grid <user-guide-ui-components-grids>`

.. image:: /completeReference/img/System/Workflows/workflows/wf_grid_actions_custom.png

- Delete the workflow: |IcDelete|

- Get to the `Edit from <../../../completeReference/Advanced/dataManagement/form.html>`_ of the workflow

.. note::

    The edit form is similar to Create form, but all the previously defined values are already filled and can be changed.
 

From the `View page <../../completeReference/Advanced/data_management/view.html>`_:

.. image:: /completeReference/img/System/Workflows/workflows/wf_view_system.png

You can deactivate, activate and clone, as well as delete the workflow and get to its Edit form with the corresponding 
action buttons in the top right corner of the page. 
 

.. |create_wf_page| image:: /completeReference/img/System/Workflows/workflows/create_wf_page.png

.. |wf_designer_step| image:: /completeReference/img/System/Workflows/workflows/wf_designer_step.png

.. |wf_designer_transition| image:: /completeReference/img/System/Workflows/workflows/wf_designer_transition.png

.. |wf_designer_transition_attributes| image:: /completeReference/img/System/Workflows/workflows/wf_designer_transition_attributes.png

.. |IcDelete| image:: /completeReference/img/common/buttons/IcDelete.png
   :align: middle

.. |IcEdit| image:: /completeReference/img/common/buttons/IcEdit.png
   :align: middle

.. |IcView| image:: /completeReference/img/common/buttons/IcView.png
   :align: middle

.. |IcActivate| image:: /completeReference/img/common/buttons/IcActivate.png
   :align: middle   
   
.. |IcDeactivate| image:: /completeReference/img/common/buttons/IcDeactivate.png
   :align: middle   
   
.. |IcClone| image:: /completeReference/img/common/buttons/IcClone.png
   :align: middle   
