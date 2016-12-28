What's new in OroCommerce Beta 3
--------------------------------

We are excited to announce that we now have a new Beta version of OroCommerce available. The new Beta 3 version adds the following features and enhancements:

**Localization**

* New localization management interface can be used to setup content and UI translation settings and formatting options for the store front-end.
* Store front-end users can now switch between the display currencies enabled in the system configuration.
* OroCommerce translation files are available for translation on Crowdin. Please join our community localization efforts to get OroCommerce translated to your language!

**Inventory**

* New inventory management UI provides an overview of the global inventory across all warehouses and it also includes export and import functions.
* It is now possible to specify primary and additional units of quantity for products.
* New default unit settings in the system configuration and the category’s “default product options” section can be used to save time during data entry.

**Catalog Management**

* It is now possible to upload multiple product images.
* SEO meta-attributes can be specified for products, categories and content pages.
* New ‘price attributes’ allow to manage product price attributes (e.g. cost, MSRP, MAP, etc.) in multiple currencies.

**Sales**

* Account users can now be easily filtered by an account that they belong to.
* Account and account user views now include grids of RFQs, quotes and orders.
* It is possible to setup an advanced RFQ notification configuration (notify the assigned sales representatives, the account or user record owners, and various combinations of thereof).

**Payments**

* The check / money order has been added to the list of the supported payment methods.
* The allowed credit card types configuration is now strictly enforced.
* Additional payment gateway configuration options (e.g. proxy settings, CVV validation, etc.) have been implemented.
* Order payment methods and statuses are now displayed in the order grids and on the order view pages on the store front-end and management console.

**Account Management**

* Account users can now manage their company address book on the store front-end (requires proper permissions).
* Open orders section provides an overview of all checkouts in progress, and allows to resume and complete an order submission.
* Admins can now hide selected user roles so that they are no longer visible in the account user role management UI on the store front-end.

**User Experience**

* We improved navigation and accessibility of the store frontend checkout.
* Product grid and view pages now include the minimum priced quantity in the quantity input boxes based on the price list settings.
* Notification messages are now stacked and follow the page when scrolled.

**Technical Improvements**

* We started to work on the frontend development guidelines. Please check the FrontendBundle documentation and provide your feedback.
* Theme assets can now be rebuild independently based on their type.
* The new layout profiler can be used to debug the generated layout of any page.
* Additional debug information (block IDs, template paths) can be injected in the page source code.
* SASS is now used as the preferred CSS pre-processor.
* DB query optimizations improved performance of selected frontend pages from 5 to 15%.

We have also included a few community contributions and more than 20 small bug fixes into this release.