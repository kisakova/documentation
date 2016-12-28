Manage your product catalog
===========================

This section describes basic concepts of the product catalog management and gives detailed guidance on the methods you can use to control the visibility and contents of OroCommerce product catalog.

Creating a Master Product Catalog
---------------------------------

To build a product catalog from scratch and fill it in with products:

     a) Create `categories and subcategories <../../completeReference/Products/MasterCatalog>`_ to form the main menu of your OroCommerce front store.

        .. image:: /completeReference/img/concepts/masterCatalogInTheStore.png
           :class: with-border
           :width: 500px

     b) If you sell products from more than one warehouse, `add all your warehouses in OroCommerce <../../completeReference/Inventory/Warehouses/create.html>`_ and `enable them in system configuration <../../completeReference/System/Configuration/Inventory/warehouses.html>`_ before `managing product inventory <../../completeReference/Inventory>`_.
     c) For every product, prepare the following information:

          i. SKU - unique product identifier.
          ii. Product name - .
          iii. Short product description - visible in the .
          iv. Detailed description - .
          
          These details are shown in the product catalog depending on the catalog view:

          * Name and SKU in the no-image view and in the gallery view:

            .. image::  /completeReference/img/concepts/product_tile.png
               :class: with-border

          * Name, SKU, and short description in the list view:

          .. image::  /completeReference/img/concepts/product_short_description.png
             :class: with-border

          * Name, SKU, short description, and description in the detailed view:

          .. image::  /completeReference/img/concepts/product_description.png
             :class: with-border

     d) `Import bulk of products <../../completeReference/commonActions/import-products>`_ to form a catalog listing. 

          i. 

          i. general info
          ii. media
          iii. price attributes
          iv. tax
     e) 
   
For a quick overview, please see the following 4 minute video:

.. raw:: html
    
    <iframe width="560" height="315" src="https://www.youtube.com/embed/0HhTC39-o6M" frameborder="0" allowfullscreen></iframe>


.. toctree::

	Organize Products Into Categories In Master Catalog <../../completeReference/Products/MasterCatalog/index>

	products_create

	../../completeReference/commonActions/import-products

	../../completeReference/Products/Products/managing-product-visibility

	../../completeReference/Products/PriceAttributes/index

	managing_product_taxation


Plan your catalog (categories, subcategories).



Product Information Management
------------------------------

Product media (images)
----------------------

Product attributes
------------------

Attribute Sets
^^^^^^^^^^^^^^

DRAFTED: Price attributes
^^^^^^^^^^^^^^^^^^^^^^^^^

Units of quantity
-----------------

Master catalog
--------------

DRAFTED: Export/import product data
-----------------------------------

Product variants
----------------

Product Variants are items that slightly vary from each other (in one or more attributes), and are presented together as a single Configurable Product for customer convenience. A product variant usually shares most of the characteristics with the main configurable product (and other variants of the same configurable product) except for the value of a several product attributes that distinguish this variant from other variants. A configurable product and all of its variants should belong to the same Product Family (so they have the same set of Product Attributes). Product variants have their own SKUs, may have they own inventory and price settings, and may generally be treated as separate products in product information management UIs.

For example, a T-Shirt may be available in various sizes and colors (e.g. Red T-Shirt XL, Red T-Shirt XXL, Green T-Shirt XL, Green T-Shirt M). In this case, the generic T-Shirt is a configurable product, Red T-Shirt XL, Red T-Shirt XXL, Green T-Shirt XL and Green T-Shirt M are product variants, and Size and Color are Configurable Attributes that define this relationship.

Configurable Attribute - is one of the Product Attributes that are used to distinguish product variants of the same configurable product from each other. There should be at least one configurable attribute specified for the configurable product in order to allow the customer to perform product variant selection.

Matrix Order Form - is a UI (UI element) that allows for ordering (specifying quantities and adding at once) of multiple product variants.

Product Type - is a property of a product that determines the way how this product's information is managed and displayed, including additional functionality available for some product types. Configurable Product and Simple Product are examples of the product types.

Simple Product - is a type of products that have their SKUs, and can be associated to Configurable Products as their product variants.

Custom personalized catalogs
----------------------------

Web categories
--------------

Landing pages & embedding product info & add to card
----------------------------------------------------

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