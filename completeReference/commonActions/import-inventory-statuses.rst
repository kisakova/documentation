Importing Inventory Statuses
============================

You can import the global product inventory statuses (In Stock, Out of Stock, or Discontinued) using the bulk import capabilities.

Import csv file should follow the high-level inventory details data structure.

**Example of inventory statuses bulk import template**

.. csv-table:: 
   :header: "SKU","Product","Inventory Status"
   :widths: 15, 15, 15

   "product.1", "Product Name", "In Stock"

.. note:: Inventory Status may be *In Stock*, *Out of Stock*, and *Discontinued*.

.. include:: /completeReference/commonActions/import.rst
   :start-after: after
   :end-before: Related Topics