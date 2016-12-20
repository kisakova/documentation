Overview
========

.. begin

Tax rules help OroCommerce find the correct tax rate that should be used for the products listed in the purchase order by matching the product tax code that indicates tax status of the product, customer tax code that indicates tax status of the buying company, and tax jurisdiction where the tax is due. OroCommerce supports tax exemption mechanism: you can set zero tax rate for some customers and/or products.

Basically, in OroCommerce, tax rule binds the following items:

* tax jurisdiction - an address, usually a state in a country that have defined taxation policies that determine when and how the company should pay their sales or VAT tax, and what rates should be used, depending on the tax status of the products you sell and  parties you sell to.

* customer tax code - a label for a customer or customer group that follow similar taxation rules in at least one tax jurisdictions.

* product tax code - a label for a group of products that have similar taxation rules in at least one tax jurisdictions.

* tax rate - the persentage of the sales income that should be payed as a tax in the particular tax jurisdiction for a certain type of products sold to a group of customers with the same tax status.

To create tax rules for a particular tax jurisdiction:

1. Create a tax jurisdiction (country, state and a range of zip codes) where a special taxation rules apply. See `Creating a tax jurisdiction </completeReference/Taxes/TaxJurisdictions/create.html>`_ for more information.

2. Create customer tax codes for every group of buyers that have fixed tax rates in this tax jurisdiction. Bind customer groups to their respective tax codes (see `Linking a tax code with a customer or customer group </completeReference/Taxes/link_tax_code_to_a_customer.html>`_).

3. Create product tax codes for every group of products that have fixed tax rates in this tax jurisdiction. Ensure that these tax codes are assigned to the products (see `Linking a tax code with a product </completeReference/Taxes/link_a_tax_code_to_a_product.html>`_).

4. Create all the tax rates defined by the tax jurisdiction for the customers you are serving and products you are selling (see `Creating a tax rate </completeReference/Taxes/Taxes/create.html>`_).

5. Finally, for every the valid combination of the tax rates, product types and customer types, create a tax rule:

  a. Naviaget to **Taxes > Tax Rules** and click **Create Tax Rule**.

  .. image:: /completeReference/img/Taxes/TaxRules/CreateTaxRule_TaxRules_Taxes_drop.png

  b. In the lists select te Account Tax Code (customer tax code), product tax code, tax jurisdiction, and tax (tax rate). Optionally, add description of the tax rate applied.

  c. Click **Save** or **Save and Close**.