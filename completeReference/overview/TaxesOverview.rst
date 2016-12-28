Tax Management Overview
=======================

.. begin

.. contents:: :local:
  :depth: 2

An international B2B selling business has certain international tax obligations, like a sales tax in the U.S. and Value Added Tax (VAT) in EU and other countries. In addition to that, some products are tax-free or have lower tax rates and some of your customers may be eligible for tax exemption. See more about `international taxes <../../completeReference/Taxes/international-taxes-overview.html>`_.

Tax management in OroCommerce helps you ensure compliance with the tax rules and regulations in global B2B online sales. With built in tax rules and tax reports you get timely and precise information for your sales tax, goods and services tax, or value added tax payment. You may inform your buyer about the volume of tax included into their order or quote, or may include the tax in the product price they see placing an order.

The following sections provide information and guidance on the following topics:

* Setting up tax rules that define the tax rate applied for a product group sold to a group of customers with similar tax obligations. The tax rate depends both on the tax jurisdiction, the tax status of your customers and the tax status of the products you are selling. When your customer files a purchase order, OroCommerce automatically picks the necessary tax rate and calculates the tax amount to be covered by your customer in this purchase order. See `Configure tax rules`_ for more information.

* Managing tax exemption: enabling zero tax rates in certain jurisdictions for the selected product categories (e.g. medical products) or customers (e.g. schools, hospitals, government organizations). See `Configure tax exemptions <../../completeReference/Taxes/managing-tax-exemptions.html>`_.

* Controlling digital product taxes. Some states in USA and the EU have special rules for taxing digital products. OroCommerce takes those regulations into account and enforces destination-based taxation when the buyer's location is in EU or in the state with no digital product tax in USA. OroCommerce distinguishes purchases of digital products b y the product tax code. All digital items should be labeled with a special tax code for digital products. Moreover, all these tax codes should be listed in EU VAT Tax and US Sales Tax configuration, to launch special tax calculation rules. See `Before you begin`_ for detailed configuration information


Before you begin
----------------

Validate the tax calculation configuration
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

By default, OroCommerce calculates tax using a rate defined in the built-in tax rule (`Configure tax rules`_) for the default shipping origin address. 

To edit configuration options that impact the way OroCommerce implies tax in the Purchase Order or Quote, navigate to **System > Configuration > Commerce > Taxation**. 

See `Configuring tax calculation <../../completeReference/System/Configuration/Taxation/tax-calculation.html>`_ topic for more information.

Set up US sales tax for digital products
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

When the digital product is purchased from the shipping origin address in the state with zero tax rate for digital products, the tax is calculated based on the shipping destination, and the global system tax calculation rules are ignored. 

To ensure that US sales tax for digital products is correctly calculated and included in your purchase quotes and orders when you sell to the US customers or from the US warehouse, label the necessary digital product tax codes in OroCommerce as taxable in US:

1. Navigate to **System > Configuration > Commerce > Taxation > US Sales Tax**.

2. Clear the **Use Default** check and click on **Choose the value**. To filter list of product tax codes, start typing the code name. The list refreshes automatically to show the values matching the text you enter. Once the necessary product code is found, select it to add to the Digital Products Tax Codes list.

3. Click **Save**.

Preview:

.. image:: /completeReference/img/System/Configuration/Taxation/USSalesTax/unlooped_Digital.gif

Set up a EU VAT tax for digital products
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
The EU VAT tax is applied when the digital good's buyer is located in EU. The tax is calculated based on the shipping destination, and the global system tax calculation rules are ignored. 

To ensure that the value added tax for digital products is included in your purchase quotes and orders from and to European Union, list all digital product tax codes in the EU VAT Tax configuration. 


The process is similar to setting digital product codes for US Sales Tax in the section above.

To configure the digital product codes that are taxable in EU: 

1. Navigate to **System > Configuration > Commerce > Taxation > EU VAT Tax**.

2. Clear the **Use Default** check and click on **Choose the value**. To filter list of product tax codes, start typing the code name. The list refreshes automatically to show the values matching the text you enter. Once the necessary product code is found, select it to add to the Digital Products Tax Codes list.

3. Click **Save**.

.. image:: /completeReference/img/System/Configuration/Taxation/EUVATtax/ConfigurationSystemTaxationEUVatTaxes.png


Configure tax rules
-------------------

Tax rules help OroCommerce find the correct tax rate for the products listed in the purchase order by matching the product tax code that indicates tax status of the product, customer tax code that indicates tax status of the buying company, and tax jurisdiction where the tax is due. OroCommerce supports tax exemption mechanism: you can set zero tax rate for some customers and products.

Basically, in OroCommerce, tax rule binds the following items:

.. image:: /completeReference/img/Taxes/TaxRules/TaxRuleIdea2.png
   :width: 50%

* tax jurisdiction - an address, usually a state in a country that have defined taxation policies that determine when and how the company should pay their sales or VAT tax, and what rates should be used, depending on the tax status of the products you sell and  parties you sell to. 

* customer tax code - a label for a customer or customer group that follow similar taxation rules in at least one tax jurisdictions.

* product tax code - a label for a group of products that have similar taxation rules in at least one tax jurisdictions.

* tax rate - the percentage of the sales income that should be payed as a tax in the particular tax jurisdiction for a certain type of products sold to a group of customers with the same tax status.


To create tax rules for a particular tax jurisdiction: 

1. Create a tax jurisdiction (country, state and a range of zip codes) where a special taxation rules apply. See `Creating a tax jurisdiction <../../completeReference/Taxes/TaxJurisdictions/create.html>`_ for more information.

2. Create customer tax codes for every group of buyers that have fixed tax rates in this tax jurisdiction. Bind customer groups to their respective tax codes (see `Linking a tax code to a customer or customer group <../../completeReference/Taxes/link-a-tax-code-to-a-customer.html>`_).

3. Create product tax codes for every group of products that have fixed tax rates in this tax jurisdiction. Ensure that these tax codes are assigned to the products (see `Linking a tax code to a product </completeReference/Taxes/link-a-tax-code-to-a-product.html>`_).

4. Create all the tax rates defined by the tax jurisdiction for the customers you are serving and products you are selling (see `Creating a tax rate </completeReference/Taxes/Taxes/create.html>`_). 
   
5. Finally, for every the valid combination of the tax rates, product types and customer types, create a tax rule:

  a. Navigate to **Taxes > Tax Rules** and click **Create Tax Rule**.

  .. image:: /completeReference/img/Taxes/TaxRules/CreateTaxRule_TaxRules_Taxes_drop.png
     
  b. Select the Account Tax Code (customer tax code), product tax code, tax jurisdiction, and tax (tax rate). Optionally, add description of the tax rate applied. 

  c. Click **Save** or **Save and Close**.
     