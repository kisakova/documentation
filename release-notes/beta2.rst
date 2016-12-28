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
