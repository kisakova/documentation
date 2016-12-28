Viewing and filtering all Templates
-----------------------------------

To view all Templates, navigate to **System > Templates** in the main menu.

Preview:

.. include:: /completeReference/overview/System/Emails/TemplatesOverview.rst
  :start-after: begin



.. image:: /completeReference/img/System/Emails/Templates/Templates.png
   :class: with-border

The following information about the Templates is available in the Templates list:

+---------------+-------------+
| Name          | Description |
+===============+=============+
| ENTITY NAME   |             |
+---------------+-------------+
| TEMPLATE NAME |             |
+---------------+-------------+
| TYPE          |             |
+---------------+-------------+
| IS SYSTEM     |             |
+---------------+-------------+

**Next steps**

You can perform the following actions with every item in the Templates list:

 * Edit

 * Clone


You can perform the following actions at the Templates page:

 * Create Email Template

:rubric: Email Templates

.. warning:: Borrowed from OroCRM. Rework.

With OroCRM you can easily sent numerous personalized emails using one template. For example, you can make a single 
template that welcomes {username}, assign it to an Email Campaign and each of your subscribers will get a mail send specifically to them. 

The articles describes the ways to create and manage Email Template records. 


.. _user-guide-email-templates-create:

Create Email Templates
----------------------

1. Go to *System → Emails → Templates* page and click :guilabel:`Create Template` button in the top right corner to 
   get to the *Create Template* page.
   
  |email_template_create|

.. |email_template_create| image:: /completeReference/img/System/Emails/Templates/marketing/email_template_create.png

2. Define the general settings of the template:

   The following fields are mandatory and **must** be defined:
  
.. csv-table::
  :header: "**Field**","**Description**"
  :widths: 10, 30

  "**Template Name***","Name used to refer to the template in the system."
  "**Type***","Use html or plain text."
  "**Owner***","Limits the list of users that can manage the template, subject to the 
  `access and permission settings <../AccessManagement>`_."
 
Optional field *"Entity Name"* shall be used to define an :term:`entity <Entity>`, variables whereof can be used 
in the template. If no entity name is defined, only system variables will be available.

.. important::

    If you want to use the template for :ref:`autoresponses <admin-configuration-system-mailboxes-autoresponse>`, the
    *"Entity Name"* value should be *"Email"*.

3. Define the email template. Click on the necessary variable to add drag it to the text box. 

.. image:: /completeReference/img/System/Emails/Templates/marketing/email_template_ex.png

4. You can click :guilabel:`Preview` button to check your template.

.. image:: /completeReference/img/System/Emails/Templates/marketing/email_template_preview.png

5. If you are satisfied with the preview, save the template in the system with the button in the top right corner of the page.

   
Email Template Languages
^^^^^^^^^^^^^^^^^^^^^^^^

If `several languages have been enabled <../../Configuration/Global/languageSettings.html>`_ for the email templates, move from tab to 
tab, to define the template in different languages.

.. image:: /completeReference/img/System/Emails/Templates/marketing/email_template_language.png

.. _user-guide-email-templates-actions:

Manage Email Templates
----------------------

The following actions are available for an email template from 
the All Email Templates page:

.. image:: /completeReference/img/System/Emails/Templates/marketing/email_template_actions.png

- Delete the template from the system: |IcDelete| 

- Edit email template: |IcEdit| 

- Clone the  template:  |IcClone| 

  You can edit the template details and save a new (cloned and edited) template.  
  
  
.. |IcDelete| image:: /completeReference/img/common/buttons/IcDelete.png
   :align: middle

.. |IcEdit| image:: /completeReference/img/common/buttons/IcEdit.png
   :align: middle
   
.. |IcClone| image:: /completeReference/img/common/buttons/IcClone.png
   :align: middle
   
.. |BGotoPage| image:: /completeReference/img/common/buttons/BGotoPage.png
   :align: middle
   
.. |Bdropdown| image:: /completeReference/img/common/buttons/Bdropdown.png
   :align: middle

.. |BCrLOwnerClear| image:: /completeReference/img/common/buttons/BCrLOwnerClear.png
   :align: middle
   