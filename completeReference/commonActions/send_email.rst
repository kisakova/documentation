.. _user-guide-activities-emails:

Send Email
==========

.. warning:: Reused from OroCRM. Rework.

Use the "*Send Email*" action to send an email from OroCRM.

The  action will be available for records of entities with the *"Emails"* activity enabled in the `entity settings <../System/Entities/entity>`_.

.. note::

    The *"Emails"* activity is by default enabled and cannot be disabled for the :term:`User` entity in OroCRM.


1. Click :guilabel:`Send Email` in the :ref:`actions <user-guide-ui-components-view-page-actions>` tab of the record.

2. The *"Send Email"* form will appear. The form has the following fields:

.. csv-table::
  :header: "**Name**","**Description**"
  :widths: 10, 30

  "**From***","The sender's address. By default, the field is filled in with the primary email address of the user, who 
  is creating the email. 
  
  To clear the field, click the :guilabel:`x` button. 
  
  If the field is clear, you can enter another email address. The field cannot be empty and only one address can be 
  defined."
  "**To, Cc and Bc**","Recipients of the email. By default, the field is filled in with the primary email address of one 
  of the contacts assigned to the record (if any).

  To clear the field, click the :guilabel:`x` button. 
   
  Click the :guilabel:`Cc` or :guilabel:`Bcc` button to define emails for a carbon copy or a blind carbon copy of the 
  email.
   
  At least one of the fields (*To*, *Cc* or *Bcc*) must be filled in."
  "**Subject***","A topic of the email. The field must be filled in."
  "**Apply template**","You can choose an `email template <../System/Emails/templates.html>`_ to use from the drop-down
  menu."
  "**Type***","Choose whether you want to use html or plain text for the email. The type is by default set to html."
  "**Body**","Define the email body."
  "**Context**","Select the records in OroCRM related to this email."
  
   
For example, we have created an email for the contact Jeffrey Maynard:

- The "From" field was automatically filled in with an email address of the user John Doe.
- The "To" field was  filled in with the email address of the contact.
- We've chosen the Happy Birthday template, which automatically defined the  subject and body. 
- This email is related to the chosen contact.  

.. image:: /completeReference/img/common/activities/send_email_ex.png  

.. hint::

    You can manually change any of the field values as required.
   
3. Click the  :guilabel:`Send` button and the email will be sent.



.. note::

    Some default email settings also depend on the `related configuration settings <../System/Emails>`_.

	
.. _user-guide-activities-emails-view:

View and Process Emails
-----------------------
All the emails sent for a record are displayed in and can be reached from the *Record Activities* section on the record details:

      |
	  
.. image:: /completeReference/img/common/activities/send_email_view.png

You can use the action icons to

- Reply to the email: |email_reply|. A form similar to the initial *Send Email* form will appear.

- Forward the email: |email_forward|.  A form similar to the initial *Send Email* form will appear.

- Define a record in OroCRM related to the email: |email_context| 
  
  
  - The *Add Context Entity* form will appear. 

  
   |
   
   |email_context_form|
  
   |
   
  - Choose the entity (account, B2B customer, etc.) from the drop-down menu and choose a specific record from the grid.

  
.. hint::

    If an email has been created from an entity record view page (e.g. from the Lead's page), this record will be added
    as a context automatically.
    
    | 
    
    |email_context_view|
    
To see the details, click on the email title or on the :guilabel:`+` to the left of it.

.. image:: /completeReference/img/common/activities/send_email_view_detailed.png


.. _user-guide-activities-emails-add-attachment:

Add Attachments
^^^^^^^^^^^^^^^

To add an attachment to the email, use the *"From Record"* and *"Upload"* links at the email form.

- Click *"Upload"* and choose the file to be attached from your computer.

- Click *"From Record"* to re-use an attachment from another email in the thread or to choose 
  an `attachment <./add_attachment.html>` assigned to the records.

.. image:: /completeReference/img/common/activities/send_email_buttons.png

.. |email_context| image:: /completeReference/img/common/activities/email_add_context.png
   :align: middle
   
.. |email_context_form| image:: /completeReference/img/common/activities/email_add_context_form.png
   :align: middle
   
.. |email_reply| image:: /completeReference/img/common/activities/email_reply.png
   :align: middle
   
.. |email_forward| image:: /completeReference/img/common/activities/email_forward.png
   :align: middle

.. |email_context_view| image:: /completeReference/img/common/activities/email_context.png
   :align: middle
