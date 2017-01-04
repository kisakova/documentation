User Guide
==========

OroCommerce User Guide introduces core capabilities of OroCommerce application and provides detailed guidance on the UI and actions available to you after you log into the application. Depending on your role in OroCommerce and custom system permissions, the actions may vary.

For detailed information on using OroCommerce, please see the following topics:

.. toctree::
   :maxdepth: 1

   install/index

   gettingStarted/index

   product/index

   inventory/index

   pricing/index

   customer/index

   quotesNProposals/index

   orders/index

   payment/index

   shipping/index

   marketing/index

   taxes/index

   support/index


For role-based information, please see the following sections:

* You are :ref:`starting a new B2B Commerce project <orocommerce-user-guide-starting>`, and plan to sell services to multiple business customers.
* :ref:`as a business owner <orocommerce-user-guide-as-a-business-owner>`
* :ref:`as a buyer <orocommerce-user-guide-as-a-buyer>`
* :ref:`as a sales person <orocommerce-user-guide-as-a-sales-person>`
* :ref:`as an organization administrator <orocommerce-user-guide-as-an-organization-administrator>`
* :ref:`as a catalog manager <orocommerce-user-guide-as-a-catalog-manager>`
* :ref:`as a system administrator <orocommerce-user-guide-as-a-system-administrator>`

.. _orocommerce-user-guide-starting:

Starting a new B2B commerce project
-----------------------------------

**WORK IN PROGRESS**

You need a complete transparency of your services for your customers, easily controlled sales and marketing process for your employees, and access to statistics and retrospective data for leadership and management team. You might start with the following:

* Request a demo (more info)
* Get a demo instance in Oro Cloud to try using OroCommerce without a hassle of complete configuration and setup. On your request, the demo instance may be installed with the demo data that reveals most of the functionality and provides the best learning experience for the new users.
* Make your mind about having an on-premise deployment vs OroCommerce in a Cloud. 
* Review a getting started section that explains basic configuration and data you'll need to start your B2B sells online.
* Plan your B2B Commerce rollover. Get more information about :ref:`using OroCommerce for Enterprize sales processes <orocommerce-user-guide-as-an-enterprise>` or about :ref:`using OroCommerce as a small and middle-size business owner <orocommerce-user-guide-as-a-business-owner>`).

.. _orocommerce-user-guide-as-a-business-owner:

Using OroCommerce as a small and middle-size business owner
-----------------------------------------------------------

**WORK IN PROGRESS**

Here is a short checklist that will help you plan and control your OroCommerce rollover:

1. Prepare OroCommerce store:

    - Install and set up OroCommerce in production mode with demo data disabled. 
    - Build a product catalog (`organize products into categories </completeReference/Products/MasterCatalog>` and :ref:`add product information manually <products_create>` or using `bulk import </completeReference/commonActions/Products/Product/import_products.html>`_).
    - Set up inventory and warehouses for your international selling services.
    - Create dedicated OroCommerce websites for locations or product lines you'd like to separate from the global store. 
    - Create global default price list to set the product prices shown in your OroCommerce store. 

2. Configure the sales process:

    - Add customers.
    - Assign sales managers to customers.
    - Configure the integrated OroCRM.
    - Configure target price lists that activate depending on the factors like active website, selected currency, buyer's location, and even on the buyer's company, e.g. you might want to offer a better deals to your partners or loyal customers.
    - Set up tax calculation rules.
    - Set up payment and delivery process (payment, shipping). **LINK**
    - Configure marketing process: `landing pages </completeReference/Marketing/LandingPages>`_, **ADD more options**.

Now your OroCommerce is ready to go. 

.. _orocommerce-user-guide-as-an-enterprise:

Using OroCommerce for Enterprise sales processes
------------------------------------------------

**WORK IN PROGRESS**

* It should scale
* More distributed decisions, approval processes, more granular set up (more websites, locales, etc.).

.. _orocommerce-user-guide-as-a-buyer:

Using OroCommerce as a buyer
----------------------------

.. include:: /guides-by-role/buyer-guide/index.rst
   :start-after: begin

.. _orocommerce-user-guide-as-a-sales-person:

Using OroCommerce as a sales person
-----------------------------------

.. include:: /guides-by-role/sales-guide/index.rst
   :start-after: begin

.. _orocommerce-user-guide-as-an-organization-administrator:

Using OroCommerce as an organization administrator
--------------------------------------------------

.. include:: /guides-by-role/org-admin-guide/index.rst
   :start-after: begin

.. _orocommerce-user-guide-as-a-catalog-manager:

Using OroCommerce as a catalog manager
--------------------------------------

.. include:: /guides-by-role/catalog-manager-guide/index.rst
   :start-after: begin

.. _orocommerce-user-guide-as-a-system-administrator:

Using OroCommerce as a system administrator
-------------------------------------------

* :ref:`Quick installation <orocommerce-user-guide-installation>`

Please, see the `Administrator Guide <../admin-guide>`_ for more detailed information about installation prerequisites, deployment sizing and configuration of third-party software.

Using OroCommerce as a system configuration manager
---------------------------------------------------

.. include:: /guides-by-role/config-guide/index.rst
   :start-after: begin

.. COMMENT -------------------------------------- This text is in the User Guide body
    * Installation
      * On Premise deployment
        * Obtain the application
        * System requirements
        * Installation wizard
      * OroCloud
        * Installation wizard / Initial configuration
          
    * Getting started
        * Navigation
        * Roles and permissions
        * Initial configuration
        * Quick start for...
            * Sales manager
            * Commerce manager
            * Oro Commerce administrator
              
    * Manage your product catalog
      * Product information management
      * Product media (images)
      * Product attributes
        * Attribute Sets
        * Price attributes
      * Units of quantity
      * Master catalog
      * Export/import product data
      * Product variants
      * Custom personalized catalogs
      * Web categories
      * Landing pages & embedding product info & add to card
      * Product visibility
        
    * Inventory
      * Overview
      * Configuration options
      * Product-level configuration
      * Working with multiple warehouses
      * Export/import inventory
        
    * Pricing
      * Overview
      * Configure prices for a website, customer group, customer
      * Scheduling
      * Export/import
      * Price attributes
      * Rule-based configuration
      * Assignment rules
      * Calculation rules
      * Working with multiple currencies
      * Price list ownership
      * Internal price lists
        
    * Customers
      * Customer accounts
      * Managing users
      * Roles and permissions
      * Account hierarchy
      * Customer groups
      * Delegate account management to customers
        
    * Quotes & Proposals
      * RFQs
        * RFQs in general + notifications
        * Default RFQ workflows (management console + store frontend)
        * Customize RFQ submission form
        * Processing RFQs, creating quotes (proposals)
          * Working with line items, etc.
        * Quote shipping
        * Quote payment term
        * Quote discounts
          
    * Order Management
      * Editing an order
      * Default order workflow (management console)
      * Default order workflow (store frontend)
      * Create an order
      * Customizing the checkout experience
        * Address books and permissions
        * Checkout workflow
        * Payment “tricks”
        * Shipping “tricks”
      * Export orders
      * Shipping tracking
        
    * Payment
      * Enabling payment methods
      * Configure payment rules
      * Payment terms
      * Payment methods:
        * Payment terms
        * PayPal Payments Pro
        * PayPal PayFlow Gateway
        * Check/Money Order
        * COD
        * Bank wire transfer
          
    * Shipping
      * Enabling shipping methods
      * Configure shipping rules
      * Product shipping attributes
      * Shipping methods:
        * Flat Rate
        * Table Rates
        * UPS
        * FedEx
        * USPS
        * ...
          
    * Marketing
      * Landing pages
      * Content blocks
      * Banners
      * Homepage
      * Promotions
        
    * Taxes
      * USA
      * Canada
      * European Union
      * Great Britain
      * Australia
      * Other counties (“get in touch with us” or refer to the partner listing page)
        
    * Support
      * Online documentation, feature videos
      * On-demand training
      * How to contact us
      * Refer to partners page
      * OroCloud customers ------------------------------------- End of User Guide body
