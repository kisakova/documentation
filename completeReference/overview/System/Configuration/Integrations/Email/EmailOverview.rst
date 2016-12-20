.. _user-guide-integrations:

OroCommerce Integrations Overview
=================================

.. warning:: Reused from OroCRM. Rework.

OroCommerce supports two types of integrations: 

- Integrations that are configured at the system level and share the same configuration for all :term:`organizations <Organization>` in an OroCommerce instance. These integrations (or any combination of them) can be enabled/disabled and configured in the *"System → Configuration → Integration"*.

  These are:

  - Pre-implemented :ref:`Google single sign-on functionality <admin-configuration-google-settings>`: Allows users to log in to OroCRM with their organization Google Apps for Work, Education or Government account, or their personal Google account if their Google account email address and OroCommerce primary email address are the same.

  - Pre-implemented :ref:`Integration with Microsoft Exchange server <admin-configuration-ms-exchange>`: Allows OroCommerce users to access contents of their mailboxes on the server directly in the OroCommerce UI. (Available for enterprise edition only).

  - Pre-implemented :ref:`Integration with Microsoft Outlook <user-guide-synch-outlook>`: Allows automatic bi-directional synchronization of the OroCommerce contacts, tasks and calendar events that are available to the users with their Microsoft Outlook applications. (Available for enterprise edition only).

.. hint::

    Along with pre-implemented integration capabilities, OroCommerce can also be integrated with other third-party systems.
