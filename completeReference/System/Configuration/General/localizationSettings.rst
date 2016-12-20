Localization
------------

Localization Options
^^^^^^^^^^^^^^^^^^^^

In *"System → Configuration → General setup → Localization → Localization Options"* you can define a number of 
localization options to be applied to the OroCRM instance, as follows:

      |
  
.. image:: /completeReference/img/System/Configuration/configuration/localization.png

.. csv-table::
  :header: "Option", "Description", "Default"
  :widths: 10, 30, 10

  "**Locale***","Affects formatting of numbers, addresses, names, and dates.","English"
  "**Primary Location*** and **Format Address Per Country***","Define the address formatting to be applied. If *Format 
  Address Per Country* is enabled and the country-specific formatting is enabled for the instance, the address will be 
  displayed in compliance with the rules specified for the country.
  For example, if the chosen country is Ukraine, the address will be displayed as follows:
  
  *ZIP code Ukraine City*
  *Street*
  *First and Last name*
  
  whereas, for the US it will be:
  
  *First and Last name*
  *Street name*
  *CITY NAME, STATE CODE, US, ZIP code*  
  Otherwise, the *Primary Location* formatting will be applied.","US" 
  "**First Quarter Starts On***","Defines the quarter start date.","January 1"
  "**Timezone***","Defines the timezone to be applied for all the time settings defined in the instance. If the 
  time-zone is changed all the time settings (e.g. due dates of :ref:`tasks <user-guide-activities-tasks>`), time of
  reminders, etc. will be changed correspondingly.","UTC +02:00"
  "**Currency***","Defines the default currency used in the system. There is no currency conversion in the system, so the
  setting basically defines the currency label applied to the monetary values defined in the system.","US dollars"
 
 
Map Options
^^^^^^^^^^^
In *"System → Configuration → General setup → Localization → Map Options"* you can define the
**Temperature Unit** and **Wind Speed Unit** used for the map displayed by the address.

The default values are Fahrenheit and miles per hour (MPH).

      |

.. image:: /completeReference/img/System/Configuration/configuration/localization_map.png

.. csv-table::
  :header: "Option", "Description", "Default"
  :widths: 10, 30, 10

  "**Locale***","Affects formatting of numbers, addresses, names, and dates.","English"
