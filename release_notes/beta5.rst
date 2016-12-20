What's new in OroCommerce Beta 5
--------------------------------

**Workflow Improvements**

* Workflows can now be fully translated, including workflow step and transition names, form attribute labels and messages.
* Built-in translation management UI allows you to use your own translation packages and allows you to customize translations locally in your system.
* Automated workflow transition triggering allows for setting up automatic transitioning using both time-based and event-based scheduling.

**Product Catalog**

* The new catalog search functionality is now available on the store front-end. The search engine takes into account all product catalog settings, including customized category and product visibility, custom pricing, and multi-language localizations. It also supports content personalization on multiple websites in OroCommerce Enterprise Edition.
* Additionally, OroCommerce Enterprise Edition users may enjoy enhanced quality of the search results, performance and scalability of the search indexing and querying via integration with the new message queue back-end (RabbitMQ) and the search index engine powered by ElasticSearch.

**Shipping & Order Management**

* Shipping rule conditions were extended to allow for creation of shipping rules using deep line item inspections (based on whether all or some line items satisfy certain conditions).
* Back-office users can now modify shipping method selections in sales orders.
* Numerous improvements have been made to the shipping integrations module (e.g. weight unit conversions, caching of shipping calculation results, option translations, etc.)

**Store Front-end**

* Major improvements (including caching, pipeline rendering of multiple page parts, sub-tree rendering and working with data) were done to the layout engine.
* We also started adaptation of the default store front-end theme to mobile device requirements (work in progress).

**Management Console**

* New improved menu management UI allows for customization of the main navigation menus for individual users, organizations (enterprise edition) or globally.
* Performance improvements in data grids that use advanced security or operation/action configurations.

**Technical Improvements**

* Improved logging module that allows for more flexibility in debugging production environments.
* New console commands to export and update workflow configuration via YAML files.
* More store front-end theme pages have been made available in the blank theme.

We have also included a few dozen of small bug fixes and miscellaneous improvements into this release.