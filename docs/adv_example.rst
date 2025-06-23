******************
Example Queries
******************

Query 1: Agricultural Research
-------------------------------

A researcher is interested in agricultural funding in IATI data, spefically in activities reported by the Food and Agriculture Organization of the United Nations (FAO). 
They visit the `IATI Registry <https://iatiregistry.org/publisher/?q=fao&sort=title+asc>`_ and determine that the organisation identifer of FAO is XM-DAC-41301.

They therefore need to search for activities with the reporting organisation reference XM-DAC-41301, using the query **Reporting Org Ref == "XM-DAC-41301"** .
Note the quotation marks around the organisation identifer.

.. figure:: images/adv_q_1.svg
    :width: 100 %
    :align: center
    :alt: Example query for IATI activities reported by the Food and Agriculture Organization of the United Nations.

    Query 1:  Activities reported by the Food and Agriculture Organization of the United Nations

If the researcher wanted to expand this search to include other reporting organisations, such the United States Department of Agriculture (US-GOV-2), they can use a comma separated list of organisation identifiers.

For example, **Reporting Org Ref == "XM-DAC-41301", "US-GOV-2"**. You can :download:`download this query <files/adv_example_q1.json>` and test it out yourself by using the "Import Query" option in advanced search.


Query 2: Humanitarian activities in Brazil
--------------------------------------------

A data user is interested in IATI activities flagged as "Humanitarian" which list Brazil as a recipient country. 

Both of these codes can be declared at activity or transaction level, so they need to create a grouped query.

Group A. will look for Humanitarian flags, declared at activity **OR** transaction level. 
Group B. will look for the recipient-country code BR for Brazil,  declared at activity **OR** transaction level. 

These groups are combined with the **AND** group operator, so the search returns results with the Humanitarian flag, **AND** Brazil as a recipient. 

This creates the query **(Humanitarian == TRUE OR Transaction Humanitarian == TRUE) AND (Recipient Country Code == BR - Brazil OR Transaction Recipient Country Code == BR - Brazil)**. 
You can :download:`download this query <files/adv_example_q2.json>` and test it out yourself by using the "Import Query" option in advanced search.

.. figure:: images/adv_q_2.svg
    :width: 100 %
    :align: center
    :alt: Example query for IATI activities flagged as "Humanitarian", which list Brazil as a recipient country.

    Query 2:  Humanitarian activities in Brazil
