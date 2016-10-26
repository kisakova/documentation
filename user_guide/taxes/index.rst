Tax Management
==============

.. contents:: :local:
	:depth: 2

Tax management concepts
-----------------------

Setting and managing taxes is a significant component of an online business’s operations, especially when expanding to international markets. Making sure your business is using the correct sales tax rules for the U.S., as well as Value Added Tax (VAT) for EU and other countries, can be a complex and error-prone operation. As an online business, you must be able to set the appropriate tax rules and rates, update and display any rate changes immediately, and collect all the necessary information to make sure your business is complying with local regulations. 

Countries all over the world apply different sales tax rates, rules, and regulations. The U.S. has a complicated tax system that includes different sales tax rates for each state, as well different tax rates for certain industries, such as communication and lodging. In addition, the seller needs to be on top of any rate changes, make sure they are maintaining exemption certificates, and are complying with their tax filings.
The picture might be even more complex in EU/non-U.S. countries, where VAT is the primary consumption tax. 

While each country has a single tax rate, the seller must track which country is collecting the tax, if the buyer or seller pays the tax, which transaction stage VAT is added, and of the multiple refund levels.

**US Sales tax**

* U.S.-based product sellers usually pay sales tax monthly, quarterly or yearly, depending on the rules set by the tax jurisdiction. 
* Companies have to apply for a sales tax permit, to legitimately pay taxes in the jurisdiction. 
* Depending on the tax jurisdiction, your company may be bound with tax obligation in the shipment origin (physical location of your warehouse storing the product you are selling), or in the selling destination - either shipment or billing address provided in the customer order.  

**European Union value added tax**

To be continued (VAT tax; VAT registration; VAT-Number validation can be executed in the VAT Information Exchange System (EU VIES) of the European Union; deduction of VAT amounts charged to them by their suppliers)...


Tax management in OroCommerce
-----------------------------

Tax management in OroCommerceo helps you ensure compliance with the tax rules and regulations in global B2B online sales. With built in tax rules and tax reports you get timely and precise information for your sales tax, goods and services tax, or value added tax payment. You may inform your buyer about the volume of tax included into their order or quote, or may hide the taxes in the product price they see placing an order. 

With OroCommerce, you can set up general tax rates for the product category, account, and tax jurisdiction. Also, to manage tax exemption,  you can enable zero tax rates in certain jurisdictions for the selected product categories (e.g. medical products) or accounts (e.g. schools, hospitals, government organizations).

Control the way taxes are calculated by setting:

* tax provider - OroCommerce built-in rules or external tax compliance service providers.

* type of base address - shipping origin, billing address, or shipping destination that defines a tax jurisdiction.

* exclusions - countries and states that use different type of address (shipping origin, billing address, or shipping destination) to defines a tax jurisdiction.

* shipping origin address.

* shipping destination (billing or shipping address).

Tax configuration
^^^^^^^^^^^^^^^^^

.. comment:: select a digital product code that requires US sales tax to be included into the Purchase Order or Quote; select a digital product code that requires EU VAT to be included into the Purchase Order or Quote; Include the tax into the product price. With this configuration, product price will be increased by the value of tax for this product item, and the purchase order will go without the Tax line. **Note**: This may complicate the tax returns and deduction for your customers (who are businesses).

.. comment:: To amend the tax calculation, use the following actions: * Change a Tax provider. By default, OroCommerce refers to the built-in tax rules (`Setting Tax Rules`_) where you configure tax rate per jurisdiction, product type and buyer's account. You can integrate external tax providers, like AvaTax or Vertex

By default, OroCommerce calculates tax using a rate defined in the built-in tax rule (`Setting Tax Rules`_) for the default shipping origin address (`Default Shipping Origin`_) .  

.. comment:: .. _Default Shipping Origin: http:// ; When disabled, Purchase Order or Quote contains zero tax rate **(???)**.  ; OroCommerce uses built-in table rates (configured)

To edit configuration options that impact the way OroCommerce implies tax in the Purchase Order or Quote, navigate to **System > Configuration > Commerce > Taxation**.

Tax calculation
~~~~~~~~~~~~~~~

.. image:: ./img/config/ConfigurationSystemTaxationTaxCalculation.png


US sales tax for digital products
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Ensure that your US sales tax for digital products is included in your purchase quotes and orders. This is extremely important when you sell to the US customers or from the US warehouse. 

To configure the digital product codes that are taxable in US:

1. Navigate to **System > Configuration > Commerce > Taxation > US Sales Tax**.
2. Clear the **Use Default** check and click on the **Choose the value** text. To filter list of product tax codes, start typing the code name. The list refreshes automatically to show the values matching the text you enter. Once the necessary product code is found, select it to add to the Digital Products Tax Codes list. 
3. Click **Save**.

Preview:

.. image:: ./img/config/unlooped_Digital.gif

.. comment:: select a digital product code that requires US sales tax to be included into the Purchase Order or Quote; 

.. comment:: Include the tax into the product price. With this configuration, product price will be increased by the value of tax for this product item, and the purchase order will go without the Tax line. **Note**: This may complicate the tax returns and deduction for your customers (who are businesses).


.. comment:: .. image:: ./img/config/ConfigurationSystemTaxationUSSalesTaxes.png


EU VAT tax for digital products
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Ensure that your US sales tax for digital products is included in your purchase quotes and orders. This is extremely important when you sell to the US customers or from the US warehouse. 

To configure the digital product codes that are taxable in US, navigate to **System > Configuration > Commerce > Taxation > US Sales Tax**.
.. comment:: select a digital product code that requires EU VAT to be included into the Purchase Order or Quote; 


.. image:: ./img/config/ConfigurationSystemTaxationEUVatTaxes.png



Enabling tax calculation
------------------------

to be continued...

Tax calculation in the customer order or quote
----------------------------------------------

To disable it:

1.  > Tax Calculation**..
2. 

Global Configuration


 - Enable
 - Tax provider (any external supported?)
 - Calculator ??? (start with/on)


 Include tax in the product price 
 System > settings > commerce > Taxation > Tax calculation 

 Tax for shipping origin or shipping destination

Setting shipping origin (in taxes???? what about multiple websites??)


US sales tax (digital products)

EU vat tax (digital products)

Configuring tax rates and rules for products 
Tax Jurisdiction (based on either shipping origin or destination, see config)
Tax rates 
Tax Rules
Special cases: tax rules for accounts (account tax code)
Special cases: tax rules for products (product tax code)


Integration with external tax management systems
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

In many cases, some of the buyers may be exempt from paying taxes or additional import fees, or a certain product may not receive any sales tax. For instance, in many countries, medical equipment can be purchased and imported tax-free. 

To take these circumstances into account when a customer is submitting an order, you should configure your tax calculation in OroCommerce to comply to the existing rules. To simplify this process, companies who use tax compliance software and services, such as Avalara or Vertex, can enable integration with these systems in OroCommerce and retrieve tax rates from those systems instead of the internal tax rules. 

.. note:: Avalara and Vertex are tax compliance management applications that help your company automatically keep up to date with the laws in each country or region in which you do business, calculate and apply any exemptions, and keep track of them for your own accounting department. 

Next steps: AvaTax connector

.. raw:: HTML

	<iframe src="https://player.vimeo.com/video/187094433?color=383838&title=0&byline=0&badge=0" width="640" height="360" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>
	<p><a href="https://vimeo.com/187094433">PRETTY FAR NORTH</a> from <a href="https://vimeo.com/pictionary">Pictionary Productions</a> on <a href="https://vimeo.com">Vimeo</a>.</p>