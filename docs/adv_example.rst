**************
Example Queries
**************

Query 1: Humanitarian activities in Brazil
-------------------

A data user is interested in IATI activities flagged as "Humanitarian" which list Brazil as a recipient country. 

Both of these codes can be declared at activity or transaction level, so they need to create a grouped query.

Group A. will look for Humanitarian flags, declared at activity **OR** transaction level. 
Group B. will look for the recipient-country code BR for Brazil,  declared at activity **OR** transaction level. 

These groups are combined with the **AND** group operator, so the search returns results with the Humanitarian flag, **AND** Brazil as a recipient. 

This creates the query **(Humanitarian == TRUE OR Transaction Humanitarian == TRUE) AND (Recipient Country Code == BR - Brazil OR Transaction Recipient Country Code == BR - Brazil)**. 
You can :download:`download this query <files/adv_example_q1.json>` and test it out yourself by using the "Import Query" option in advanced search.

.. figure:: images/adv_q_1.svg
    :width: 100 %
    :align: center
    :alt: Example query IATI activities flagged as "Humanitarian", which list Brazil as a recipient country.

    Query 1:  Humanitarian activities in Brazil

