Managing product visibility
^^^^^^^^^^^^^^^^^^^^^^^^^^^

While *a product* on *a website* for *a customer* can be either *visible* or *hidden*, the way OroCommerce evaluates the product visibility might seem tricky.

.. note:: Administrator should have permissions to view the account, account groups, and websites to have access to the settings described in this section.

Whether the product is shown to the customer on the OroCommerce website depends on the following configuration:
 * `Visibility to Account`_: is the product/category visible to the user's organization or business unit (account)?
 * `Visibility to Account Group`_: is the product/category visible to the group of accounts? Accounts may be grouped based on the authentication or type of business accounts are in.
 * `Visibility on the Website`_: is the product visible to the account (or account group) on the website? Multiple websites might be useful to split the content and settings for different target customer locations.

Additionally, there are default visibility settings that may be easily inherited in the above configuration:
 * `System Configuration`_ (system-wide)
 * `Visibility to All`_ (per product/category).

**Visibility options**

Generally, these are available visibility settings:

 * *visible* - show the product in the catalog on the customer-facing website
 * *hidden* - hide the product from the catalog on the customer-facing website
 * *config* - inherit the visibility that is defined in the `System Configuration`_ for users of all accounts
 * *product* - use the option that is selected in the `Visibility to All`_ section for the product
 * *category* - use the option that is selected in the `Visibility to All`_ section for the product's category
 * *parent* - use the option that is selected in the `Visibility to All`_ section for the parent master catalog category 
 * *account group* - use the option that is selected in the `Visibility to Account Group`_ the customer is in

**Visibility priorities**

Categories visibility has higher priority over the product visibility. If the category is hidden, the product will not be visible and the visibility will be overridden.

Visibility for account group overrides visibility for an account.

Navigation to visibility settings
=================================

**In Product**: Navigate to **Products > Products** (system menu), select a product to customize its visibility, and click **Manage visibility** on the top right (product menu).

**In Category**: Navigate to **Products > Master Catalog** (system menu), select a category on the left and scroll to the **Visibility** section.

**In System Configuration**: Open **System > Configuration** in the main menu. Select **Commerce > Account > Visibility** on the left.

Default settings
================

System Configuration
--------------------

You can define a system-wide products and categories visibility for customers of the existing accounts. This setting applies whenever visibility is set to 'config'.
 
Products and categories are visible by default. To change this, navigate to system configuration by opening **System > Configuration > Commerce > Account > Visibility**, untick 'Use default' and toggle the options (hidden/shown).

.. image:: ./img/productVisibility/systemConfProductVisibility.png
   :align: center

Visibility to All
-----------------

Default visibility for product or category is configured in the product's *Manage visibility* page and in the category details, *Visibility* section. 

Possible options are:

 * (parent) category - inherit configuration from the parent category
 * config - inherit settings from the `System Configuration`_
 * hidden
 * visible 
  

These values may be later inherited or enforced by visibility for accounts and account groups set to 'product' or 'category'.

.. image:: ./img/productVisibility/visibilityToAll.png
  :align: center

Direct settings
===============

Visibility to Account Group
---------------------------

You can control if the product or category is shown to the customers who are members of the account group.  Use one of the following options:

 * product - inherit configuration from the product
 * category - inherit configuration from the parent category
 * hidden
 * visible

By default, the new account group inherits the default product visibility from the product or category (depending on where the configuration happens).

  .. image:: ./img/productVisibility/visibilityToAccountGroups.png
    :align: center

Visibility to Account
---------------------

Visibility to the account supports same options as `Visibility to Account Group`_ and can also inherit the configuration for account group (by default).

  .. image:: ./img/productVisibility/visibilityToAccounts.png
    :align: center

Visibility on the Website
-------------------------

Every product can have customized visibility for the particular website. This might be necessary when a product requires special government permit in a particular country. A seller might hide it on the country's local website until the paperwork is complete.

On the product visibility page, you can switch between the websites and apply the necessary changes. 

.. image:: ./img/productVisibility/prodVisibility.png
  :align: center

For new websites, the following default settings apply:

 * Visibility to all inherits visibility config of the category product is in.
 * Visibility to account group (user groups in the account) inherit visibility configuration on the product level.
 * Visibility to account inherits settings for the (account group).   