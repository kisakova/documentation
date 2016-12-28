Creating Account Users
======================

To create an account user, the seller-admin should navigate to the customer tab located in the top menu and click on “Account Users.” The first thing the seller will see are all the account users already entered into the system. He can easily edit these by selecting a specific record and clicking edit.

Admin account user view- Account Users - Customers

.. image:: /completeReference/img/System/UserManagement/Customer/admin-account-user.png
   :class: with-border

To create a new record, the seller should click on the blue button labelled “Create Account User.” The image below shows some of the fields the seller needs to fill out in order to create the account (fields can easily be added or deleted using configuration files), including which account this user will belong to, their password, their role, etc. If there are no roles are available yet, the seller can just save this record and come back when at least one role is available in the system.

Admin Create Account User 1- Account Users - Customers

.. image:: /completeReference/img/System/UserManagement/Customer/admin-create-account-user.png
   :class: with-border

Create a User Record
--------------------

In order to create a :term:`User` record:

- Go to *System → User Management → Users*
- Click the :guilabel:`Create User` button
- Define the user settings in the sections described below.


General
^^^^^^^

The "General" section defines the basic settings of the user created. The following fields are mandatory and **must** be 
defined in the section.

.. csv-table::
  :header: "**Name**","**Description**"
  :widths: 10, 30

  "**Owner**","Define a :term:`business unit <Business Unit>`, users of which can manage the user, subject to the `role settings <../roles.html>`_."
  "**Status**","Chose the record status. Possible values are *Inactive* or *Active*."
  "**Username**","The name used to log into the system (login)."
  "**Password**","The password used to log into the system."
  "**First Name** and **Last Name**","Name used to refer to the user in the UI."
  "Primary Email","Email associated with the user in the system."
  
Along with the mandatory fields, there are a number of optional fields provided by default, that can be used to define 
additional details of the customer, such as the name prefix and suffix, the middle name, birthday, additional emails,
and phone number. You can also add the avatar (upload a picture to be used for the user in the UI) and/or 
:term:`tags <Tag>` related to the user.

The "*Send An Email Invitation*" check-box defines whether an invitation email must be sent to the user. The email 
content is defined in the course of the system integration and cannot be edited from the UI.

      |
  
.. image:: /completeReference/img/System/UserManagement/user_management/user_general.png


Additional
^^^^^^^^^^
  
Any :ref:`custom fields added <user-guide-field-management-create>` to the "User" entity can be defined in the 
*"Additional"* section.

Groups and Roles
^^^^^^^^^^^^^^^^

The "Groups and Roles" section contains all the `user groups <../groups.html>`_ and 
`roles <../roles.html>`_ available in the system. Check the boxes to assign the user
created to a group/role.

One user may have several roles. All the permissions granted to at least one of the roles, are granted to the user. 

      |
 
.. image:: /completeReference/img/System/UserManagement/user_management/user_groups.png


Access Settings
^^^^^^^^^^^^^^^

The "Access Settings" section contains all the `organizations <../organizations.html>`_ and 
`business units <../business-units.html>` available in the system. Check the boxes to assign the user
to an organization/business unit.

.. image:: /completeReference/img/System/UserManagement/user_management/user_access.png

.. hint::

    In the community enterprise there can only be one organization, so organizations are not shown in the structure.

.. _user-management-users-email-sync:

Email synchronization settings
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Use the section to synchronize emails between mailbox of the user and OroCRM. 

- Let OroCRM know the details (such as host, port, and encryption) of IMAP to upload the incoming mail to OroCRM 
- Define the SMTP details (such as host, port, and encryption) to synchronize the outgoing mail from OroCRM to the 
  mailbox
- Specify the login (user) and password used to access the mailbox
- Click the :guilabel:`Check Connection/Retrieve Folders` 
- After successful connection, the list of available folders will be loaded. Check the Folders to be synchronized.

In the example below, synchronization has been done for a .gmail mailbox. The INBOX folder will be synchronized.


.. hint::

    Detailed instructions on the way to set-up IMAP and SMTP connection in gmail, are provided 
    `here <https://support.google.com/mail/troubleshooter/1668960?hl=en&rd=1#ts=1665018%2C1665144>`_

    To enable connection, check the box next to
    `Allow access for less secure apps box <https://support.google.com/accounts/answer/6010255?hl=en>`_


.. image:: /completeReference/img/System/Configuration/General/system_mailbox/synchronize_mb.png 
