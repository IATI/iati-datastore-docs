****************************
Simple Search: User Guide
****************************

The home page of `Datastore Search <https://datastore.iatistandard.org/>`_ contains the “Simple Search” bar. This performs a text search on every narrative element within IATI activity data. 

For a summary of all elements in the standard, please see the `Activity Standard Summary Table <https://www.google.com/url?q=https://iatistandard.org/en/iati-standard/203/activity-standard/summary-table/&sa=D&source=docs&ust=1733222605142915&usg=AOvVaw1so5C1Bi3cyCOvJ2ziPKKk>`_.

Search operators
-------------------

Simple search includes search operators; special commands that make your search more precise. 
These operators and examples of their use are documented below:


.. csv-table::
    :file: tables/search_operators.csv
    :widths: 10, 45, 45
    :header-rows: 1

Downloading Results
-------------------

You can download the results of your search in different levels of detail and formats.

Levels:
    - **Activity level:** each row in the data represents one activity. This can contain many transactions and budgets.
    - **Transaction level:** each row represents one transaction. Activity level information is repeated for each transaction.
    - **Budget level:** each row represents one budget. Activity level information is repeated for each budget.

Formats:
    - **XML:** A valid IATI standard XML file containing all the results from your search. This format can only describe activity-level data.
    - **JSON:** A flattened Javascript representation of your search results.
    - **CSV:** A flattened, comma separated export of your search results. Fields with multiple values are combined into a comma separated list. To note: in this format, cell lengths can exceed the Microsoft Excel limit of 32,767 characters.
    - **EXCEL:** A flattened, comma separated export of your search results, modified to be compatible with Microsoft Excel. Fields with multiple values are combined into a pipe (|) separated list. Cell values longer than 32,767 characters are truncated to 32,700 characters.

Advanced Search
-------------------

If you want to expand a simple search to include non narrative elements, click the "Advanced" button on the results page. 
This will open the advanced search menu, auto-populated with your existing search. 
See :ref:`adv_search` for more information. 


