FAQs
To be edited:

Why is data missing from Datastore Search?
The IATI Datastore contains all IATI data known to the IATI Registry which is both version 2.0 or above and conforms to the IATI XML Schema. 
Files that do not conform to the IATI XML schema are marked as critically invalid in the IATI Validator

Data formats?

All valid IATI data (i.e. data that conforms to the IATI XML Schema) is available in JSON, CSV and XML formats.
Users can query IATI data on all elements and attributes contained in the Standard.

All IATI data can be queried and returned in one of three CSV formats:
One activity per row
One transaction per row
One budget per row

How do I search for a specific phrase or identifier?
To search for a particular phrase, use quotation marks. For example, "rabbit production" will return search results about rabbit production, where as rabbit production will return results about rabbits, and results about production. For more information on how to use the Datastore Search, please see the User Guide.

Data cleaning?
The IATI Datastore indexes and represents IATI data precisely as it is was originally published, with no transformations or layers of inferred meaning or metadata.


4c. Validation

Only valid IATI activities are imported into the IATI Datastore. If an activity is marked as a critical error in the IATI Validator, it will not appear in Datastore Search.