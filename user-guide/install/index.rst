.. _orocommerce-user-guide-installation:

Installation
============

This section contains the information necessary for OroCommerce deployment planning and execution.

Before you begin
----------------

Architecture overview
~~~~~~~~~~~~~~~~~~~~~

**Brief (expand):** OroCommerce runs on the Application Server (e.g. Apache) and connects to the Database Server (e.g. MySQL). Set up for fault tolerance and load balancing...

Types of deployment
~~~~~~~~~~~~~~~~~~~

You can install OroCommerce either on premises, on the servers hosted in your company infrastructure, or in the Oro Cloud, on the servers hosted in the Google Cloud 
(coming soon). Installation steps depend on the type of the deployment and selected base operation system.

Software requirements
~~~~~~~~~~~~~~~~~~~~~

**Server**

+-----------------------------+-----------------------------------------------------------------------------------------------------------------------+
| Type                        | Description                                                                                                           |
+=============================+=======================================================================================================================+
| Operating System            | * Linux x86, x86-64                                                                                                   |
|                             | * Windows 7 and 8                                                                                                     |
|                             | * Mac OS X 10.9 and above                                                                                             |
+-----------------------------+-----------------------------------------------------------------------------------------------------------------------+
| Browsers                    | * Mozilla Firefox 6 and above                                                                                         |
|                             | * Google Chrome 31 and above                                                                                          |
|                             | * Microsoft Internet Explorer 10 and above                                                                            |
|                             | * Safari                                                                                                              |
|                             | * Opera 12.16 and above                                                                                               |
+-----------------------------+-----------------------------------------------------------------------------------------------------------------------+
| Web Servers                 | * Apache 2.2.x                                                                                                        |
|                             | * Nginx                                                                                                               |
|                             | * Lighttpd                                                                                                            |
+-----------------------------+-----------------------------------------------------------------------------------------------------------------------+
| Database Management Systems | * MySQL 5.1 and above                                                                                                 |
|                             | * PostgreSQL/EnterpriseDB 9.1 and above                                                                               |
+-----------------------------+-----------------------------------------------------------------------------------------------------------------------+
| Other                       | * PHP 5.5.9 and above                                                                                                 |
|                             | * PHP composer (application-level package manager)                                                                    |
|                             | * PHP Command Line Interface                                                                                          |
|                             | * PHP extensions:                                                                                                     |
|                             |                                                                                                                       |
|                             | - ctype                                                                                                               |
|                             | - fileinfo                                                                                                            |
|                             | - GD 2.0 and above                                                                                                    |
|                             | - intl                                                                                                                |
|                             | - JSON                                                                                                                |
|                             | - Mcrypt                                                                                                              |
|                             | - PCRE 8.0 and above                                                                                                  |
|                             | - SimpleXML                                                                                                           |
|                             | - Tokenizer                                                                                                           |
|                             |                                                                                                                       |
|                             | * PHP settings:                                                                                                       |
|                             |                                                                                                                       |
|                             | - date.timezone must be set                                                                                           |
|                             | - detect_unicode must be disabled in php.ini                                                                          |
|                             | - memory_limit should be at least 512M                                                                                |
|                             | - xdebug.scream must be disabled in php.ini                                                                           |
|                             | - xdebug.show_exception_trace must be disabled in php.ini                                                             |
|                             | - ICU library 4.4 and above                                                                                           |
|                             | - mcrypt_encrypt() should be available                                                                                |
|                             |                                                                                                                       |
|                             | * File and folder permissions:                                                                                        |
|                             |                                                                                                                       |
|                             | - web/bundles/ directory must be writable                                                                             |
|                             | - web/uploads/ directory must be writable                                                                             |
+-----------------------------+-----------------------------------------------------------------------------------------------------------------------+
| Optional                    | * Node.js (for JS minification)                                                                                       |
|                             | * PHP-XML module installed                                                                                            |
|                             | * xdebug.max_nesting_level above 100 in php.ini                                                                       |
|                             | * iconv() available ◦mb_strlen() available                                                                            |
+-----------------------------+-----------------------------------------------------------------------------------------------------------------------+
|                             | * posix_isatty() available                                                                                            |
|                             | * utf8_decode() available                                                                                             |
|                             | * Tidy PHP extension should be installed to make sure that any HTML is correctly converted into a text representation |
+-----------------------------+-----------------------------------------------------------------------------------------------------------------------+

**Client**

+----------+--------------------------------------------+
| Type     | Description                                |
+==========+============================================+
| Browsers | * Mozilla Firefox 6 and above              |
|          | * Google Chrome 31 and above               |
|          | * Microsoft Internet Explorer 10 and above |
|          | * Safari                                   |
|          | * Opera 12.16 and above                    |
+----------+--------------------------------------------+

Hardware requirements
~~~~~~~~~~~~~~~~~~~~~

**Brief (expand):** Please refer to your application server and database server hardware requirements. (ToDo: Add OroCommerce benchmark info) 

On Premise deployment
---------------------

Obtain the OroCommerce distribution files
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

**Brief (expand):** Clone git repository or get an archived copy from your sales representative. 

Prepare environment for deployment
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

**Brief (expand):** Hosts, networking, ports considerations. parameters.yml file. Installation checklist. Database creation. 

1. Install the database server
2. Create a dedicated user for OroCommerce connection to the database server.
3. Create a dedicated database for OroCommerce.
4. Install the application server.
5. Copy the distribution files into the application server host and set up the necessary web application access and visibility permissions.
6. To install the distribution package dependencies, in the distribution package root, run the following command: `COMPOSER=dev.json composer install -dmemory_limit=-1 --prefer-dist --optimize-autoloader --no-dev --no-interaction in your *Commerce* application directory)`.

Now you are ready for OroCommerce installation.

Install OroCommerce
~~~~~~~~~~~~~~~~~~~

Silent Installation
^^^^^^^^^^^^^^^^^^^

To install OroCommerce in a silent mode:

* In the distribution package, locate the parameters.yml file and provide information for database, network, mail server, and security configuration that will be used during the installation. See `Sample of Parameters.yml file`_ for more information.
* Once you are done with parameters configuration, run the following command replacing the items in bold with the information specific to your deployment.

.. code-block:: bash

	php -dxcache.cacher=0 **<distribution_files_local_folder>**/commerce/app/console oro:install 
	        --application-url=**<localhost/oro>**
	        --env=prod
	        --user-name=**admin**
	        --user-email=**admin@example.com**
	        --user-firstname=**John**
	        --user-lastname=**Doe**
	        --user-password=**admin**
	        --sample-data=**y**
	        --organization-name="**Acme, Inc**"
	        --force
	        --timeout=10000

.. note:: Use *--sample-data=y* only for learning purposes, test deployments and pre-production deployments. In this mode, OroCommerce is populated with sample data that help you unlock all the features so that you can quickly test the system after re-configuration or customization.

Sample of Parameters.yml file
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. code-block:: xml

    # This file is auto-generated during the composer install (updated dtabase_user and password)
	parameters:
	    database_driver: pdo_mysql
	    database_host: 0.0.0.0
	    database_port: null
	    database_name: b2b_dev
	    database_user: admin
	    database_password: ~
	    mailer_transport: mail
	    mailer_host: 127.0.0.1
	    mailer_port: null
	    mailer_encryption: null
	    mailer_user: null
	    mailer_password: null
	    websocket_bind_address: 0.0.0.0
	    websocket_bind_port: 8080
	    websocket_frontend_host: '*'
	    websocket_frontend_port: 8080
	    websocket_backend_host: '*'
	    websocket_backend_port: 8080
	    web_backend_prefix: /admin
	    session_handler: session.handler.native_file
	    locale: en
	    secret: ThisTokenIsNotSoSecretChangeIt
	    installed: null
	    assets_version: cfc43f2f
	    assets_version_strategy: time_hash
 

Installation in a Web UI
^^^^^^^^^^^^^^^^^^^^^^^^

1. In web browser, open the following URL: *http://<ApplicationServerHost>:<ApplicationServerPort>/install.php*
2. Click Begin Installation on the Welcome to Oro Installer screen.
3. On the *System requirements check* step, ensure that system requirements are met (status indicators should be green for all items) and click **Next**.
4. On the *Configuration* step, provide the following information:

     a) For *Database connection*:
     		* provide a driver (either MySQL, or PostgreSQL), 
     		* enter the database server host and port, 
     		* enter the database name (*Name*), user name and password for OroCommerce authentication with the database server.
     		* For re-installation, specify whether OroCommerce should remove existing database table contents. Available options are *None*, *Application Tables*, *All Tables*. Default value is *None*.
     b) In *System settings*, specify the system language and the secret for OAuth 2 client authorization. 
     c) In *Web settings*, provide the prefix that will be attached to the application URL to access the OroCommerce configuration and administration application (backend).
     d) In *Mailer settings*, select the transport for the emails OroCommerce will be sending. Available options are *PHP mail*, *SMTP*, and *sendmail*. When you select the *SNMP*, please, provide the following mail server connection details: host, port, encryption (None, SSL, TLS), user name, and password.
     e) In the *Websocket connection*, set up your web service network configuration: service bind address and port, WS backend and frontend host/post.
     f) Once you are happy with the information you've provided, click **Next**.

5. The *Database initialization* will automatically start.  Click **Next** when the status of all steps turn green.
6. On the *Administration* step, provide the following information:

     a) Organization name
     b) Application URL (e.g. http://commerce.MyCompany.com)
     c) Create a first system administrator by providing a user name, password (with confirmation), email, and their fist and last name.
     d) If necessary, tick *Load Sample Data* box. 
     e) Finally, click **Install** and wait until the status for all operations turns green. Once installation is complete, click **Next**. 

     .. note:: Load Sample Data only for learning purposes, test deployments and pre-production deployments. In this mode, OroCommerce is populated with sample data that help you unlock all the features so that you can quickly test the system after re-configuration or customization.

7. On the *Finish* step, click **Launch Application** to open the OroCommerce Administration Login screen. The URL will usually be: *http://<hostname>:<port>/app.php/admin/user/login*. To login, use credentials you provided for the first system administrator.

Installation Walk-through
^^^^^^^^^^^^^^^^^^^^^^^^^

See this short demo of the installation in the web UI:

.. raw:: HTML

   <video controls src="_static/OroCommerceInstallation.mp4"></video>

OroCloud
--------