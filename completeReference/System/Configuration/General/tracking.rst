Tracking
--------

The Tracking section specifies the settings to be applied for all the 
tracking records created in the system.

The following options are available:

.. csv-table::
  :header: "Option", "Description", "Default"
  :widths: 10, 30, 10
  
  "**Enable Dynamic Tracking***","If enabled, tracking data will be processed in the real-time mode. Please note, this 
  may affect the performance.","Enabled"
  "**Log Rotation Interval***","Defines how often log files must be processed if the *Dynamic Tracking* is 
  disabled.","1 hour"
  "**Piwik Host**","The field must be specified if you want the tracking date to be sent to a
  Piwik account. The value corresponds to the Piwik analytics URL of your account.","None"
  "**Piwik Token Auth**","The field must be specified if you want the tracking date to be sent to a
  Piwik account. The value corresponds to the Piwik `token_auth <http://piwik.org/faq/general/faq_114/>`_ field.","None"

.. caution::

    In order to enable the data transfer to a Piwik account, the "identifier" field of the Tracking Website record shall
    be the same as the `Website ID <http://piwik.org/faq/general/faq_19212/>`_ used by Piwik.

At the bottom of the form there is a link to the grid of all the Tracking Website records.

.. note:: Reuse OroCRM's Tracking Websites! 