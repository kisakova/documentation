Contributing to Documentation
=============================

.. contents:: :local:

We use `reStructuredText`_ markup language to write the documentation and `Sphinx`_ generator to prepare it for the web publication at http://www.orocrm.com/documentation. You can find more information about the syntax on the Sphinx website by reading `reStructuredText Primer`_. The most inposrtant information is provided in the sections below.

Documentation source files are maintained in the dedicated `gitgub <https://github.com/orocommerce/documentation>`_ repository.

If you are willing to contribute - you are totally welcome. The information below should help with understanding documentation structure and topic organization, useful rst directives and a simple workflow that helps quickly publish a new topic.

Before You Begin
----------------

Before submitting your documentation changes in a pull request, please sign our `Contributor License Agreement`_ (CLA). The CLA must be signed for any code or documentation changes to be accepted.

.. _Contributor License Agreement: http://www.orocrm.com/contributor-license-agreement

Fork Documentation Project
--------------------------

If you're just making a small change, you can use the "Edit this file" button directly in the GitHub UI. It will automatically create a fork of our documentation repository and allow for the creation and submission of a new pull request with your modifications once you are done editing:

* `OroPlatform and OroCRM documentation <https://github.com/orocrm/documentation>`_
* `OroCommerce documentation <https://github.com/orocommerce/documentation>`_

For large volume of  updates, fixes, and enhancements please use the following process: 
#. `Fork <https://help.github.com/articles/fork-a-repo>`_ a documentation repository.

#. `Clone <https://help.github.com/articles/cloning-a-repository/>`_ the forked repository.

#. Update your local copy of documentation (see `Update Documentation`_ for more information on the process and formatting).

#. Build and test the documentation before submitting the pull request to be sure you haven't accidentally introduced any layout or formatting issues.

  .. note::

   To build Sphinx documentation, set up a local Sphinx build environment:

      * Install `Sphinx`_.        
      * Install the required Sphinx extensions: ``git submodule update --init``.

   To test your changes before you commit them, run ``make html`` and check the generated documentation in the ``_build`` directory.

.. _reStructuredText:        http://docutils.sourceforge.net/rst.html
.. _Sphinx:                  http://sphinx-doc.org/

Update Documentation
--------------------

This section is intended to provide you with basic information of simple text formatting using reStructuredText (reST) markup language. Just enough to update and create new documetnation files in OroCommerce documentation.

For more information, please refer to the sphinx's `reStructuredText Primer`_ and to the `Quick reStructuredText <http://docutils.sourceforge.net/docs/user/rst/quickref.html>`_ by `docutils <http://docutils.sourceforge.net>`_.

The most complete information is available in the `reStructureText specificaion <http://docutils.sourceforge.net/docs/ref/rst/restructuredtext.html>`_.

.. _reStructuredText Primer: http://sphinx-doc.org/rest.html

Documentation Structure and Topic Organization
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

In OroCommerce, documentation is organized into the tree hierarchy of sections using toctree directive in the index.rst. Sections of the same level recide in the same folder which simplifies navigation and sibling reference.

Sample file structure:

.. code-block:: none

    + user_guide:
        + img:
            - Demo.png
        - topic-1.rst
        - topic-2.rst
        - topic-3.rst
        - index.rst
    + admin_guide:
        - index.rst
        + integration
            - email.rst
            - LDAP.rst
    + img:
        - Architecture.png
    - index.rst

Basic Rst Syntax
^^^^^^^^^^^^^^^^

Headings
~~~~~~~~

Use the following markup for the headings split your topic into secions, subsections, and more granular bits:

Use an underline with =, -, ^, ~, " to mark up the sections.

.. code-block:: none

    Section 1
    =========

    Section 1.1
    -----------

    Section 1.1.1
    ^^^^^^^^^^^^^

    Section 1.1.1.1
    ~~~~~~~~~~~~~~~

    Paragraph Title
    """""""""""""""

Preview:

.. image:: /completeReference/img/common/write.png

Preserve the same level of indentation for all lines of the paragraph. More information is available `here <http://docutils.sourceforge.net/docs/ref/rst/restructuredtext.html#paragraphs>`_.

Inline Markup
~~~~~~~~~~~~~

Surround the text with one asterisk (\*) for *italic* text, with two asterisks (\*\*) for **bold** text, and with double backquotes (\`\`) for ``Preformatted`` text. to use these symbols in the text without affecting the text style, escape them with the backslash (\\).

Bulleted List
~~~~~~~~~~~~~

To form a bullet list, start the line with \*, +, or \- followed by whitespace:

.. code-block:: none

    * Item A
    * Item B

        - Item C
        - Item D
          
            + Item E
            + Item F

Preview:

* Item A
* Item B

    - Item C
    - Item D
          
            + Item E
            + Item F

Numbered List
~~~~~~~~~~~~~

To form a numbered list, start the line with arabic numerals (1,2,3), upper- or lowercase alphabet letters (A,B,C, or a,b,c), upper- or lowercase Roman numerals (I, II, III, or i, ii, iii). You can automatically enumerate the list by starting the lines with a hash sign (\#).

Simple numbered list:

.. code-block:: none

    1. Item A
    2. Item B

         a) Item C
         b) Item D

              i. Item E
              ii. Item F


Preview:

1. Item A
2. Item B

         a) Item C
         b) Item D

              i. Item E
              ii. Item F

Autoenumerated List
~~~~~~~~~~~~~~~~~~~

.. code-block:: none

    1. Item A
    #. Item B

         a) Item C
         #) Item D

              i. Item E
              #. Item F

Preview:

1. Item A
#. Item B

         a) Item C
         #) Item D

              i. Item E
              #. Item F


Text Blocks
~~~~~~~~~~~

+-----------+------------------------------------+----------------------------------+
| Block     | Syntax                             | Preview                          |
+===========+====================================+==================================+
| Attention | \.\. attention:: The message text. | .. attention:: The message text. |
+-----------+------------------------------------+----------------------------------+
| Caution   | \.\. caution:: The message.        | .. caution:: The message.        |
+-----------+------------------------------------+----------------------------------+
| Warning   | \.\. warning:: The message.        | .. warning:: The message.        |
+-----------+------------------------------------+----------------------------------+
| Hint      | \.\. hint:: The message.           | .. hint:: The message.           |
+-----------+------------------------------------+----------------------------------+
| Note      | \.\. note:: The message.           | .. note:: The message.           |
+-----------+------------------------------------+----------------------------------+
| Tip       | \.\. tip:: The message.            | .. tip:: The message.            |
+-----------+------------------------------------+----------------------------------+
| Important | \.\. important:: The message.      | .. important:: The message.      |
+-----------+------------------------------------+----------------------------------+

Tables
~~~~~~

.. code-block:: none

    +------------+------------+-----------+
    | Header 1   | Header 2   | Header 3  |
    +============+============+===========+
    | Cell 1.1   | Cell 1.2   | Cell 1.3  |
    +------------+------------+-----------+
    | Cell 2.1   | Cell 2.2   | Cell 2.3  |
    +------------+------------+-----------+

Preview:

+------------+------------+-----------+
| Header 1   | Header 2   | Header 3  |
+============+============+===========+
| Cell 1.1   | Cell 1.2   | Cell 1.3  |
+------------+------------+-----------+
| Cell 2.1   | Cell 2.2   | Cell 2.3  |
+------------+------------+-----------+

Advanced Rst Syntax
^^^^^^^^^^^^^^^^^^^

Temporarily, the information resides `on Confluence <https://magecore.atlassian.net/wiki/display/OD/RST+syntax+in+Oro+Documentation>`_. 

.. note:: References to the section titles in the doc are enbabled with the 'sphinx.ext.autosectionlabel' plugin.

.. TODO: complete this section (move from confluence to github)


Add a New Topic
^^^^^^^^^^^^^^^

1. Create topic contents using Restructured Text format and save the file using the following filename convention: 

    * Use lowercase letters for the name.

    * Remove whitespaces or replace them with a dash symbol ('-'), if necessary.

    * Avoid special symbols (/,$,#, etc) that may cause issues in the filename.

    * Save the file with .rst extension

2. To link a topic to the global documentation table of contents:

    a) Identify the best location for the reference to your new topic in the documentation structure.
    b) Move the newly created file to the selected folder. 
    c) Append the relative focument name (without the rst extension) to the toctree definition in the potential parent topic. 

For example, when we create a new topic with additional information about pricelist management in the *additional_pricelist_management_info.rst* file. To include it into the document structure at the **user_guide/pricing** level, we'll update the *index.rst* file in the *user_guide/pricing* directory like in the following example:

**Before:**

.. code-block:: none

    .. toctree::
       :maxdepth: 1

       price_attributes

       price_list_management

**After:**

.. code-block:: none

    .. toctree::
       :maxdepth: 1

       price_attributes

       price_list_management

       additional_pricelist_management_info

Submit Documentation Updates
----------------------------

Once you are ready, create a pull request in the `OroCommerce documentation <https://github.com/orocommerce/documentation>`_ repository with changes from your forked repository.

After documentation review, your changes will be merged to the OroCommerce documentation and will be published on the `OroCommerce website <http://www.orocommerce.com/documentation>`_