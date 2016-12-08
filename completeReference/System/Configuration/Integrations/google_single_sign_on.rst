Google Single Sign-On Integration
=================================

OroCommerce can use Google Single Sign-On capabilities to provide simplified user authentication. When a user is already logged into their google account, their session will start without the login prompt.

This topic provides guidance on the following steps:

.. contents:: :local:

Preparing for Google Single Sign-On integration
-----------------------------------------------

To prepare for Google Single Sign-On (Google SSO) integration, register your OroCommerce deployment with Google providing the URLs in your OroCommerce instance for Authorized JavaScript origins and Authorized redirect URIs. Use the following procedure:

1. Open `Google Developers Console <https://console.developers.google.com/start>`_:

2. Click **Create project** in the **Projects** list on the top left.

3. Give you project a name, answer the questions on the form, and click **CREATE**.

4. In the newly created project, click **Credentials** on the left:
   
   a) Navigate to the **OAuth consent screen** section and configure the message that is shown to OroCommerce users before their first login using Google SSO: provide product name (e.g. OroCommerce for ACME) and homepage URL (e.g. https://orocommerce.acme.com), and prodcut logo URL.

   b) Navigate to the **Credentials** section, then click **Create credentials** and select **OAuth client ID** from the list.

   c) Select **Web application** as application type.

   d) Fill in the application name (e.g. OroCommerce for ACME), Authorized JavaScript origins, and Authorized redirect URIs.

      .. note::
           In Authorized JavaScript origins, put the URL of your OroCommerce instance that will use a Google single sign-on.

           In Authorized redirect URIs, put the following two values:

              * [URL of your OroCommerce instance]/login/check-google

              * [URL of your OroCommerce instance]/app.php/login/check-google

   e) Click :guilabel:`Create` button.

   f) Your OAuth client ID and secret is generated and displayed in a pop-up. Note them down, as you will need them during integration configuration in OroCommerce.

   g) Click **OK**. 

Enabling Google Single Sign-On
------------------------------

To enable Google SSO integration:

1. Navigate to the **System → Configuration** section using main menu, then navigate to the **Integrations → Google Settings** in the menu to the left.

2. Enter the OAuth client ID and secret generated in Google Developer's Console (step f in the previous section).

3. In the Google Single Sign-On section:

   a) Set **Enable** option.

   b) Optionally, provide the list of domains to keep Google Single Sign-On available exclusively for the users with emails from these domains.

4. Click :guilabel:`Save Settings` button.
   
.. TODO: check what OAuth 2.0 for email sync does when enabled. 

Using Single Sign-On
--------------------

.. warning:: Reused from OroCRM. Rework.

.. TODO: improve.

When a user gets to the login page of an instance for which single sign-on capability has been enabled, there is a **login using Google** link. 

- If the user is not logged in to any Google accounts, after the link has been clicked, a usual Google log-in page appears.

  |
    
- After the user has logged in to the Google account, a request to use the account in order to log-in to OroCRM will 
  appear. (Details defined for the consent screen will be used).

  |
  
  |PermissionAccept|

  |
  
  By clicking Accept, you allow this app and Google to use your information in accordance with their respective terms of 
  service and privacy policies. You can change this and other Account Permissions at any time.

For now on, for a user logged-in into a Google account, it is enough to click the *"login using Google"* link to get
into OroCRM.

.. important::

    The email used for the Google account and the primary email of the user in OroCRM must be the same.
  
  

.. |CreateProject| image:: /completeReference/img/System/Configuration/Integrations/google_integration/create_project.png
   :align: middle
   
.. |APImenu| image:: /completeReference/img/System/Configuration/Integrations/google_integration/apis_menu.png
   :align: middle
   
.. |ConsentScreen| image:: /completeReference/img/System/Configuration/Integrations/google_integration/consent_screen.png
   :align: middle
   
.. |CreateClientID| image:: /completeReference/img/System/Configuration/Integrations/google_integration/create_client_id.png
   :align: middle
   
.. |CreateClientIDForm| image:: /completeReference/img/System/Configuration/Integrations/google_integration/create_client_id_form.png
   :align: middle
   
.. |OroGoogleSettings| image:: /completeReference/img/System/Configuration/Integrations/google_integration/oro_google_settings.png
   :align: middle
   
.. |PermissionAccept| image:: /completeReference/img/System/Configuration/Integrations/google_integration/permission_accept.png
   :align: middle   
