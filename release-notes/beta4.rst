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

* OroCommerce Enterprise Edition users can run and manage multiple websites  (store frontend) on a single OroCommerce installation.
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