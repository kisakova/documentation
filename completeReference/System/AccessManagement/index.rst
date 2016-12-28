User Access Management in OroCommerce
=====================================

.. contents:: :local:
    :depth: 3

A user's ability to access data and perform actions in the system depends on the following:

*  User role: E.g., sales manager and system administrators need access to different data and system capabilities.

   - Actions a user can perform with particular data depend on access levels set for these actions in the user's role.
   
   - Roles also control access to certain parts of the system. 
   
   Therefore, for some users interface may not always look like on the images in this guide. 

   Users can check their role on the **My User** page. 

*  Organizations and units which the user has access to or has membership in, e.g., users who work in different divisions have access to the data within their division. This information is available on the **My User** page.  

|   
	   
.. image:: /completeReference/img/System/UserManagement/access_roles_management/user_access.png 

|

*  Ownership for particular data: some information may be a part of a business unit, division, or organization level. Data ownership creates this relation and help isolate the information based in the ownership (e.g. customer's A owner is a business unit B, whose user B created the customer A record and set onwership to their business unit). Some data may be bound to the particular ownership type (for example, company address book may belong only to the whole company and the ownership may not be limited to the individual user, business unit or division.
  
   Users who create or edit a record can specify a record owner. The range from which they can pick up a record owner depends on the user role(s) and the ownership type of an entity the record they create / edit.  


Related Information
-------------------

* `Role Management </completeReference/System/UserManagement/roles.html>`_. 

* `Access Level </completeReference/System/AccessManagement/access_configuration.html>`_.

* User Access to `Business Units </completeReference/System/UserManagement/business-units.html>`_ and Organizations </completeReference/System/UserManagement/organizations.html>`_.

* Altering available access levels for the entity by setting `Ownership Type </completeReference/System/AccessManagement/ownership.html>`_.

* `Sample access configuration </completeReference/System/AccessManagement/example.html>`_.


.. toctree::
    :hidden:

    ../UserManagement/roles

    ownership

    access-configuration

    example

    user-access-settings