Tax Management
==============

.. contents:: :local:
	:depth: 2

An international B2B selling business has certain international tax obligations, like a sales tax in the U.S. and Value Added Tax (VAT) in EU and other countries. In addition to that, some products are tax-free or have lower tax rates and some of your customers may be eligible for tax exemption.

.. note:: **International taxes overview**

        Countries all over the world apply different sales tax rates, rules, and regulations. The U.S. has a complicated tax system that includes different sales tax rates for each state, as well different tax rates for certain industries, such as communication and lodging. In addition, the seller needs to be on top of any rate changes, make sure they are maintaining exemption certificates, and are complying with their tax filings. The picture might be even more complex in EU/non-U.S. countries, where VAT is the primary consumption tax.
        
        While each country has a single tax rate, the seller must track which country is collecting the tax, if the buyer or seller pays the tax, which transaction stage VAT is added, and of the multiple refund levels.
        
        **US Sales tax**
        
        * U.S.-based product sellers usually pay sales tax monthly, quarterly or yearly, depending on the rules set by the tax jurisdiction.

        * Companies have to apply for a sales tax permit, to legitimately pay taxes in the jurisdiction.

        * Depending on the tax jurisdiction, your company may be bound with tax obligation in the shipment origin (physical location of your warehouse storing the product you are selling), or in the selling destination - either shipment or billing address provided in the customer order.

        **European Union value added tax**

        * To be continued (VAT tax; VAT registration; VAT-Number validation can be executed in the VAT Information Exchange System (EU VIES) of the European Union; deduction of VAT amounts charged to them by their suppliers)...

Tax management in OroCommerce helps you ensure compliance with the tax rules and regulations in global B2B online sales. With built in tax rules and tax reports you get timely and precise information for your sales tax, goods and services tax, or value added tax payment. You may inform your buyer about the volume of tax included into their order or quote, or may include the tax in the product price they see placing an order.

The following sections provide information and guidance on the following topics:

* Configuring tax calculation in OroCommerce (e.g. setting base tax jurisdictions, calculation and display methods, etc). See `Tax calculation`_ section for more information.

* Setting up tax rules that define the tax rate applied for a product group sold to a group of customers with similar tax obligations. The tax rate depends both on the tax jurisdiction, the tax status of your customers and the tax status of the products you are selling. When your customer files a purchase order, OroCommerce automatically picks the necessary tax rate and calculates the tax amount to be covered by your customer in this purchase order. See `Managing tax rules`_ for more information.

* Managing tax exemption: enabling zero tax rates in certain jurisdictions for the selected product categories (e.g. medical products) or customers (e.g. schools, hospitals, government organizations). See `Managing tax exemptions`_.

* Controling digital product taxes: provide a list of digital product codes to group all digital products and services that are sold in United States of America and European Union using OroCommerce. Digital products are taxed unlike other products and services, and OroCommerce takes these exceptions into account. See ...??? and ...??? for more information.


Tax calculation
---------------

By default, OroCommerce calculates tax using a rate defined in the built-in tax rule (`Managing tax rules`_) for the default shipping origin address.

To edit configuration options that impact the way OroCommerce implies tax in the Purchase Order or Quote, navigate to **System > Configuration > Commerce > Taxation** and perform the necessary configuration:

- Enable or disable tax calculation for the products you sell.

- Select a tax provider. OroCommerce build-in Table Rates (the tax rules defined in `Managing tax rules`_ section) are used by default. Alternatively, with some customization, you can use external tax management and compliance system, like AvaTax or Vertex, as a tax provider. See `Integration with external tax management systems`_ for more information.

- Apply taxes per single item in the purchase order or per total for the requested amount of the items of same kind. This may minimize roundoff accumulated error and secure you and your customers from over or under paying.

- Configure how OroCommerce selects the core jurisdiction whose tax rules should be applied in a purchase order tax calculation. Tax jurisdiction may be defined by either shipping origin, billing address, or shipping destination.

- Set up any tax jurisdiction exceptions - countries and states where tax jurisdiction selection should deviate from the core rule. For example, when the main tax jurisdiction is at the sale shipping destination, the exception may be for some countries and states to use shiping origin instead.
  
- Decide wheather the tax is included into the product price. When this option is enabled, the product price displayed in the purchase order will increase by the value of tax for this product item. **Note**: This may complicate the tax returns and deduction for your customers who are businesses.

- Configure a shipping origin address that will be used system-wide for origin-based tax. When the shipping origin is a core jurisdiction, OroCommerce will use the address provided here to find the matching built-in tax jurisdiction rules for tax calculation.  

 _`Taxes` **link goes here!!!**

Sample configuration for tax calculation
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. image:: ./img/config/ConfigurationSystemTaxationTaxCalculation.png

Available actions:

.. note:: Remember to clear the **Use default** flag before setting a custom option. 

1. In **Enable Taxation** section, enable or disable taxation by setting or clearing the **Enabled** box. 

2. In **Tax Provider** section, keep the default **Built-in Table Rates** or, if you have extended the default capabilities and set up an integration, select your custom tax management system.   

4. In **Calculator** section:

  a. With **Start Calculation With**, specify the formula for tax calculation. Tax is calculated either for unit price or for a product total price. Formula for *Unit price* is:

    | tax = [ ( unit price * tax rate ) * unit quantity ] + ... + [ ( unit price * tax rate ) * unit quantity ].  

    Formula for *Row Total* is:

    | tax = [ (unit price * unit quantity) * tax rate ] + ... + [ (unit price * unit quantity) * tax rate ].

  b. With **Start Calculation On** option, select when the rounding off shall happen. For **Item**, the taxable ammount is rounded up for every item. For **Total**, the total tax is aggregated as is, and the final amount is rounded up.
   
  c. Set or clear the **Product prices include tax** option. When product prices include tax, the tax ammount is substructed from unit, product, or total price. Otherwise, the tax is added on top of the unit, product, or total price.

4. In **Matcher** section:
   
   a. Select the default tax jurisdiction base:
  
    * For origin-based jurisdiction, select **Shipping Origin**, or

    * For destination-based jurisdiction, select **Destination**.

   b. Specify all countries and states/regions that do not follow the default tax jurisdiction base. Click **+ Add**, select a country, type in state or region and select the alternative tax jurisdiction base.
   
   c. If you use destination as tax jurisdiction base by default or for any exclusions, select either **Shipping Address** or **Billing Address** as **Destination**.
      
5. In **Origin** section, provide the origin address (e.g. location of your warehouse or company legal address). For the origin-based jurisdictions, OroCommerce uses this address to find the matching tax rule.


US sales tax for digital products
---------------------------------

Ensure that your US sales tax for digital products is included in your purchase quotes and orders when you sell to the US customers or from the US warehouse.

To label digital product codes in OroCommerce as taxable in US:

1. Navigate to **System > Configuration > Commerce > Taxation > US Sales Tax**.

2. Clear the **Use Default** check and click on **Choose the value**. To filter list of product tax codes, start typing the code name. The list refreshes automatically to show the values matching the text you enter. Once the necessary product code is found, select it to add to the Digital Products Tax Codes list.

3. Click **Save**.

Preview:

.. image:: ./img/config/unlooped_Digital.gif

EU VAT tax for digital products
-------------------------------

Ensure that the value added tax for digital products is included in your purchase quotes and orders from and to European Union. 

The process is similar to setting digital product codes for US Sales Tax in the section above.

To configure the digital product codes that are taxable in EU: 

1. Navigate to **System > Configuration > Commerce > Taxation > EU VAT Tax**.

2. Clear the **Use Default** check and click on **Choose the value**. To filter list of product tax codes, start typing the code name. The list refreshes automatically to show the values matching the text you enter. Once the necessary product code is found, select it to add to the Digital Products Tax Codes list.

3. Click **Save**.

.. image:: ./img/config/ConfigurationSystemTaxationEUVatTaxes.png


Managing tax rules
------------------

Tax rules help OroCommerce find the correct tax rate that should be used for the products listed in the purchase order by matching the product tax code that indicates tax status of the product, customer tax code that indicates tax status of the buying company, and tax jurisdiction where the tax is due. OroCommerce supports tax exemption mechanism: you can set zero tax rate for some customers and/or products.

Basically, in OroCommerce, tax rule binds the following items:

* tax jurisdiction - an address, usually a state in a country that have defined taxation policies that determine when and how the company should pay their sales or VAT tax, and what rates should be used, depending on the tax status of the products you sell and  parties you sell to. 

* customer tax code - a label for a customer or customer group that follow similar taxation rules in at least one tax jurisdictions.

* product tax code - a label for a group of products that have similar taxation rules in at least one tax jurisdictions.

* tax rate - the persentage of the sales income that should be payed as a tax in the particular tax jurisdiction for a certain type of products sold to a group of customers with the same tax status.
  
To create tax rules for a particular tax jurisdiction: 

1. Create a tax jurisdiction (country, state and a range of zip codes) where a special taxation rules apply. See `Creating a tax jurisdiction`_ for more information.

2. Create customer tax codes for every group of buyers that have fixed tax rates in this tax jurisdiction. Bind customer groups to their respective tax codes (see `Linking a tax code with a customer or customer group`_).

3. Create product tax codes for every group of products that have fixed tax rates in this tax jurisdiction. Ensure that these tax codes are assigned to the products (see `Linking a tax code with a product`_).

4. Create all the tax rates defined by the tax jurisdiction for the customers you are serving and products you are selling (see `Creating a tax rate`_). 
   
5. Finally, for every the valid combination of the tax rates, product types and customer types, create a tax rule:

  a. Naviaget to **Taxes > Tax Rules** and click **Create Tax Rule**.

  .. image:: ./img/tax_rules/CreateTaxRule_TaxRules_Taxes_drop.png
     
  b. In the lists select te Account Tax Code (customer tax code), product tax code, tax jurisdiction, and tax (tax rate). Optionally, add description of the tax rate applied. 

  c. Click **Save** or **Save and Close**.
     
Managing tax jurisdictions
~~~~~~~~~~~~~~~~~~~~~~~~~~

Viewing tax jurisdictions
^^^^^^^^^^^^^^^^^^^^^^^^^

.. image:: ./img/jurisdiction/LOS_ANGELES_COUNTY_View_TaxJurisdictions_Taxes.png

.. image:: ./img/jurisdiction/All_TaxJurisdictionsTaxes.png

Creating a tax jurisdiction
^^^^^^^^^^^^^^^^^^^^^^^^^^^


Editing a tax jurisdiction
^^^^^^^^^^^^^^^^^^^^^^^^^^
.. image:: ./img/jurisdiction/LOS_ANGELES_COUNTY_Edit_TaxJurisdictions_Taxes.png


Filtering tax jurisdictions
^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. image:: ./img/jurisdiction/Taxes_TaxJurisdiction_TaxFilter_Dates.png

.. image:: ./img/jurisdiction/Taxes_TaxJurisdiction_TaxFilter_Code.png


Managing tax rates
~~~~~~~~~~~~~~~~~~

.. image:: ./img/taxes/All_Taxes_Taxes.png

.. image:: ./img/taxes/LOS_ANGELES_COUNTY_SALES_TAX_Edit_Taxes_Taxes.png

.. image:: ./img/taxes/LOS_ANGELES_COUNTY_SALES_TAX_View_Taxes_Taxes.png

Creating a tax rate
^^^^^^^^^^^^^^^^^^^

.. image:: ./img/taxes/CreateTax_Taxes_Taxes.png


Managing customer tax codes
~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. image:: ./img/account_tax_codes/FOREIGNGOVERNMENTSViewAccountTaxCodesTaxes1.png

.. image:: ./img/account_tax_codes/AllAccountTaxCodesTaxes.png

.. image:: ./img/account_tax_codes/CreateAccountTaxCodeAccountTaxCodesTaxes.png

.. image:: ./img/account_tax_codes/FOREIGNGOVERNMENTSEditAccountTaxCodesTaxes.png

Linking a tax code with a customer or customer group
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. image:: ./img/taxes_from_account_view/AccountTaxCode_view.png

.. image:: ./img/taxes_from_account_view/AccountTaxCode_view_ fromAccountGroup.png

.. image:: ./img/taxes_from_account_view/AccountTaxCode_edit.png

.. image:: ./img/taxes_from_account_view/AccountTaxCode_edit_cropped.png

.. image:: ./img/Taxes_Tax_Actions.png

Managing product tax codes
~~~~~~~~~~~~~~~~~~~~~~~~~~

taxes_from_product_view

.. image:: ./img/taxes_from_product_view/ProductTaxCode.png

.. image:: ./img/taxes_from_product_view/ProductTaxCode_view.png

product_tax_code

.. image:: ./img/product_tax_code/CreateProductTaxCode_ProductTaxCodes_Taxes.png

.. image:: ./img/product_tax_code/All_ProductTaxCodes_Taxes.png

.. image:: ./img/product_tax_code/MEDICAL_IDENTIFICATION_TAGS_Edit_ProductTaxCodes_Taxes.png

.. image:: ./img/product_tax_code/MEDICAL_IDENTIFICATION_TAGS_Edit_ProductTaxCodes_Taxes1.png

.. image:: ./img/product_tax_code/MEDICAL_IDENTIFICATION_TAGS_View_ProductTaxCodes_Taxes_ChangeHistory.png

.. image:: ./img/product_tax_code/MEDICAL_IDENTIFICATION_TAGS_View_ProductTaxCodes_Taxes.png

Linking a tax code with a product
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Viewing tax rules
^^^^^^^^^^^^^^^^^

List:

.. image:: ./img/tax_rules/All_TaxRules_Taxes.png

A:
.. image:: ./img/tax_rules/1View_TaxRules_Taxes.png

Creating a new tax rule
^^^^^^^^^^^^^^^^^^^^^^^

.. image:: ./img/tax_rules/CreateTaxRule_TaxRules_Taxes.png

.. image:: ./img/tax_rules/CreateTaxRule_TaxRules_Taxes_drop.png

Editing tax rule
^^^^^^^^^^^^^^^^

.. image:: ./img/tax_rules/1Edit_TaxRules_Taxes.png


Managing tax exemptions
-----------------------

Tax exempt customers
~~~~~~~~~~~~~~~~~~~~


Tax exempt products
~~~~~~~~~~~~~~~~~~~


Viewing tax in the purchase order
---------------------------------

ToDo

Integration with external tax management systems
------------------------------------------------

In many cases, some of the buyers may be exempt from paying taxes or additional import fees, or a certain product may not receive any sales tax. For instance, in many countries, medical equipment can be purchased and imported tax-free.

To take these circumstances into account when a customer is submitting an order, you should configure your tax calculation in OroCommerce to comply to the existing rules. To simplify this process, companies who use tax compliance software and services, such as Avalara or Vertex, can enable integration with these systems in OroCommerce and retrieve tax rates from those systems instead of the internal tax rules.

.. note:: Avalara and Vertex are tax compliance management applications that help your company automatically keep up to date with the laws in each country or region in which you do business, calculate and apply any exemptions, and keep track of them for your own accounting department. 

Next steps: AvaTax connector

.. raw:: HTML

	<iframe src="https://player.vimeo.com/video/187094433?color=383838&title=0&byline=0&badge=0" width="640" height="360" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>
	<p><a href="https://vimeo.com/187094433">PRETTY FAR NORTH</a> from <a href="https://vimeo.com/pictionary">Pictionary Productions</a> on <a href="https://vimeo.com">Vimeo</a>.</p>
