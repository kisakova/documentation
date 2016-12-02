Contribute to Writing Documentation
===================================

Open-source OroCommerce documentation is written in ReStructured Text format (.rst files) and html and pdf output is built using the `Sphinx <http://www.sphinx-doc.org/>`_.

Documentation source files are maintained in the dedicated `gitgub <https://github.com/orocommerce/documentation>`_ repository.

If you are willing to contribute - you are totally welcome. The information below should help with understanding documentation structure and topic organization, useful rst directives and a simple workflow that helps quickly publish a new topic.

Documentation Structure and Topic Organization
----------------------------------------------

Sample file structure:

.. code-block:: none

    user_guide:
        img:
            Demo.png
        topic-1.rst
        topic-2.rst
        topic-3.rst
        index.rst
    admin_guide:
        index.rst
        integration
            email.rst
            LDAP.rst
    img:
        Architecture.png
    index.rst

Basic Rst Syntax
----------------

Advanced Rst Syntax
-------------------

Temporarily, the information resides `here <https://magecore.atlassian.net/wiki/display/OD/RST+syntax+in+Oro+Documentation>`_. 

Publishing a New Topic
----------------------

Create a topic
^^^^^^^^^^^^^^

Create a new rst file in one of the folders using the following filename convention: 
* Use lowercase letters for the name.
* Remove whitespaces or replace them with a dash symbol ('-'), if necessary.
* Avoid special symbols (/,$,#, etc) that may cause issues in the filename.
* Save the file with .rst extension

Link topic to the Table of Contents
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Identify the best location in the documentation structure for the reference to your new topic. 

E.g. additional information about pricelist management will natuirally fit into the **user_guide/pricing** section. 

**FIXME: incomplete**