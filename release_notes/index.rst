Release notes
=============

.. contents:: :local:

What's new in OroCommerce Beta 4
--------------------------------

**Price Management**

* Ability to use product and category attributes to define rules for price calculations and their applicability in the price lists (e.g. calculate price based on the product purchase price, add the maximum margin that was set on the product or category level, and apply discounts for the customer group that this price list is created for, not exceeding the defined minimum margin).
* Now you can use another price list for price calculations as well (e.g. calculate prices in the wholesale price list based on the prices from the default price list and include additional discount for quantities over 10,000 items, not exceeding the minimum sale price/margin defined for the products).

**Shipping**

* New shipping rule engine allows for extremely flexible and powerful configuration of available shipping options based on the shopping cart contents, product attributes, inventory availability and location, shipping destination and customer account information.
* We added UPS shipping integration (including support for multiple shipping accounts and independent configuration for different geographies).

**Localization**

* It is now possible to upload your own translation files in addition to translations that are offered via Crowdin. Please join our community localization efforts to get OroCommerce translated to your language!
* New translation management UI provides a way to translate application from within the admin UI.
* Multiple languages can be enabled on the store frontend to allow customers to choose the language with the language switcher.

**Workflow Engine**

* Workflow engine now allows to have multiple workflows for a single entity to be active at the same time.
* It is now possible to start and transition entity through different workflows separately, based on the entity contents or other conditions.
* It is no longer necessary to create separate entities, their supporting database structures and UIs just for the purpose of enabling an alternative workflow.

**Multiple Websites**

* OroCommerce Enterprise Edition users can run and manage multiple store frontends (websites) on a single OroCommerce installation.
* Different websites can be made available to users based on the domain, URL, cookies, server environment variables, and can be further extended to support geolocation and automatic language detection.
* Each website can be configured separately (themes, layouts, availability of the store frontend features and their configuration, product availability and pricing, checkout experience and other business processes).

**Job Queue**

* New job queue implementation allows for asynchronous scheduling, reliable execution and independent scaling of resource consuming operations.
* Product and catalog visibility updates now use the new job queue implementation.
* Price list updates and recalculations now use the new job queue implementation.

**Application Management**

* New ‘feature toggles’ module allow to easily manage application features (turn them on and off, along with the related configuration settings) both for the management console and for the store frontend.
* OroCommerce Enterprise Edition users can use feature toggles to enable/disable features in the context of selected organizations and websites.
* RFQ (request for quote) functionality can be turned off on the store frontend websites on for the management console users.

**User Experience**

* It is now possible to see and quickly edit products that have been added to multiple shopping list right from the product listing page.
* Order history grid includes more order details.
* We added another sample theme for the store frontend to show developers how to enable and efficiently reuse multiple themes. We also included a blank theme with minimalistic styling for the developers who prefer to use their own approach for styles and assets organization.
* A new store frontend homepage is another example of how a page content can be customized in a frontend theme.
* Account user permissions have been organized into separate groups to simplify account user role management in the management console.

**Payments**

* Quote (proposal) can now include the payment term that will be honored during checkout and order submission.
* Customers can be allowed to use PayPal account balance to pay for their purchases on the store frontend.


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


What's new in OroCommerce Beta 2
--------------------------------

We are moving fast forward towards OroCommerce General Availability (GA) release and today we reached yet another mile stone. We are excited to announce that we now have a new Beta version of OroCommerce available. This new Beta 2 version adds the following features enhancements and technical improvements:

**Feature Enhancements**

**Price list**

* Price list management functionality has been expanded to allow for scheduling price list activation and deactivation (multiple time intervals are supported, as well as open-ended time period definition).
* A price list can also be temporarily disabled if necessary.
* Admins can now copy entire price list with prices in just a single click.

**Store front**

* Store frontend users may now see all their incomplete orders (checkouts) in progress, and switch between them as necessary. The users with additional permissions may see, review and complete order submission on behalf of other users within their corporate account.
* The store frontend can now be made available to guest users. We are working on additional configuration options, feature toggles and SEO capabilities.
* It is now possible to check all available product price tiers right in the product list. The user can also see the price he will receive for the specified quantity and unit of measurement without adding the product to the shopping list.
* Product listing page now also indicates quantities of the product that have already been added to the shopping list. We are working additional configuration options and a new design of this customer time-saving functionality.
* It is now possible to show products without prices on the store frontend (for example, product may have no price visible to a specific customer group, or customer account). Such products can still be added to a shopping cart, and customers will have to request a quote to see pricing and complete the order submission

**Purchasing Process**

* Zero amount authorization can be enabled by a merchant to validate credit cards without posting an authorization balance hold until the order submission.
* Customers may now allow their credit card to be used for subsequent orders.
* Quotes are now automatically marked as expired, and customers cannot accept a quote past its expiration date.

**Shipping**

* It is now possible to specify shipping origin in system configuration or for individual warehouses.
* Product shipping options (weight, dimensions, freight class) can now be configured on the product edit screen.

**Technical Improvements**

* Delete operations are now automatically added to the main entity management grids. It is no longer necessary to write any code to implement regular deletion. Standard delete operation can be disabled for specific grids.
* Grid sorting, pagination and error handling have been improved on the product inventory management screen.
* Admin menu was rearranged to provide easier access to frequently used functions.
* Styling and handling of notifications, validation hints, error messages and other common elements have been improved to simplify their customization.
