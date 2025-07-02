API
===

An API is available with methods to query the datastore from your code and get results programatically.

To use this, you must sign up for an API key. 

The `Developer website <https://developer.iatistandard.org/>`_ allows you to get a key and gives you details of the API methods you can call and their parameters.

The rest of this page describes details of the API and should be read alongside the `Developer website <https://developer.iatistandard.org/>`_.

Field names and content in activity collection
----------------------------------------------

Field names are constructed from the the XML tag and (if applicable) the attribute. For example field names you can query include:

* sector_percentage
* sector_vocabulary
* sector_code
* sector_narrative

These all come from the :iati-reference:`sector` element of the standard.

As the :iati-reference:`sector` element can appear multiple times in an activity, the contents of these fields can be a list of all the values that appear in the activity.

Here is an example:

* `"sector_code":["16050","3","10"]`
* `"sector_percentage":[100.0,50.0,50.0]`
* `"sector_vocabulary":["1","7","7"]`

It is not possible to tell from these lists which element in one field applies to an element in another list.

For example, you can't tell which code is from which vocabulary or which percentage applies to which code. (You may be able to guess from context in this example, but you can't tell for sure).


Field names and content in transaction and budget collection
------------------------------------------------------------

In these collections, one data item is returned for each transaction or budget. 

Any field names that start with the name of that collection come from that item only.

Any other field names come from the actvity and include all data in the activity. This makes it easy to construct complex queries.

For example, on an activity collection result you may see these fields:

* `"transaction_value":[10954.0,14086.0]`
* `"transaction_value_value_date":["2023-03-05T00:00:00Z","2023-08-15T00:00:00Z"]`
* `"sector_code":["16050","3","10"]`
* `"sector_percentage":[100.0,50.0,50.0]`
* `"sector_vocabulary":["1","7","7"]`

However on the transaction collection you will get one result with:

* `"transaction_value":[14086.0]`
* `"transaction_value_value_date":["2023-08-15T00:00:00Z"]`
* `"sector_code":["16050","3","10"]`
* `"sector_percentage":[100.0,50.0,50.0]`
* `"sector_vocabulary":["1","7","7"]`

And a second result with:

* `"transaction_value":[10954.0]`
* `"transaction_value_value_date":["2023-03-05T00:00:00Z"]`
* `"sector_code":["16050","3","10"]`
* `"sector_percentage":[100.0,50.0,50.0]`
* `"sector_vocabulary":["1","7","7"]`

Getting other data formats back from the activity collection
------------------------------------------------------------

You can pass `iati_xml` to the `fl` paramaeter to get back a string of the XML of the activity.

You can pass `iati_json` to the `fl` parameter to get back a JSON representation of the XML, with structure.

Here is a truncated example with the same sector data as the above example:

.. code-block:: json

    {
    "iati-activity": [
        {
        "@last-updated-datetime": "2024-11-27T11:23:09+01:00",
        "@xml:lang": "fr",
        "iati-identifier": [
            {
            "text()": "AB-123-123-123-123"
            }
        ],
        "sector": [
            {
            "@vocabulary": "1",
            "@code": "16050",
            "@percentage": "100"
            },
            {
            "@vocabulary": "7",
            "@code": "3",
            "@percentage": "50"
            },
            {
            "@vocabulary": "7",
            "@code": "10",
            "@percentage": "50"
            }
        ]
        }
    ]
    }

Unlike the flattened lists returned in previous examples, in this example it is possible to tell which sector code relates to which percentage and which vocabulary.



