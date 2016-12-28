View and Manage a User
----------------------

All the users available are displayed in the Users grid
(*System → User Management → Users*).

From the grid you can:


- Delete a user from the system: |IcDelete|.

- Get to the `Edit form <../../../completeReference/Advanced/dataManagement/form.html>`_ of the user: |IcEdit|.

- Get to the `View page <../../../completeReference/Advanced/data_management/view.html>`_ of the user: |IcView|.

User View Page
^^^^^^^^^^^^^^

View page of a user record contains the following sections:

      |

Action Buttons
~~~~~~~~~~~~~~

With the :ref:`action buttons <user-guide-ui-components-view-page-actions>` on the View page you can:
  
- Perform the actions available enable for the user entity in the 
  :ref:`Communication &  Collaboration settings <user-guide-entity-management-create-commun-collab>` (e.g. Assign Tasks,
  Send Emails etc.)
  
- Reset Password: The user will be prompted by email to reset their password and will be disabled from login until
  they do so.

- Change Password: Create new password (administrator will know this new password). The user will be notified on the 
  change by email.

.. image:: /completeReference/img/System/UserManagement/user_management/reset_password.png

General Information
~~~~~~~~~~~~~~~~~~~

The section contains basic details of the user, namely:

- Username
- Birthday
- Emails
- Phone number
- Roles assigned to the user
- Groups the user belongs to
- Business unit the user belongs to
- Any custom fields :ref:`added <user-guide-field-management-create>` to the "User" entity will appear in the order 
  defined by their :ref:`priority <user-guide-entity-management-other-common>`.
  
Activities
~~~~~~~~~~

The section contains all the `activities <../../../commonActions/actions.html>`_ related to the user.

Additional Information
~~~~~~~~~~~~~~~~~~~~~~

The section contains details of the :ref:`tasks <user-guide-activities-tasks-assign>` assigned to the user.

.. |IcDelete| image:: /completeReference/img/common/buttons/IcDelete.png
   :align: middle

.. |IcEdit| image:: /completeReference/img/common/buttons/IcEdit.png
   :align: middle

.. |IcView| image:: /completeReference/img/common/buttons/IcView.png
   :align: middle