# Search

*  When you update or create a record, the search engine comes along, makes a copy of the data, and breaks up the content into smaller pieces called tokens. We store these tokens in the search index, along with a link back to the original record.

*  When users enter a term in the search field (1), the search engine breaks up the search term into tokens (2). It matches those tokens to the record information stored in the search index (3), ranks the associated records by relevance (4), and returns the results that users have access to (5).

*  SOQL query is the equivalent of a SELECT SQL statement and searches the org database. 
*  Query (REST) and query() (SOAP)—Executes a SOQL query against the specified object and returns data that matches the specified criteria.

*  SOSL is a programmatic way of performing a text-based search against the search index.
*  Search (REST) and search() (SOAP)—Executes a SOSL text string search against your org’s data.


*  Use SOQL when you know in which objects or fields the data resides and you want to:
      * Retrieve data from a single object or from multiple objects that are related to one another.
      * Count the number of records that meet specified criteria.
      * Sort results as part of the query.
      * Retrieve data from number, date, or checkbox fields.

```
* Use SOSL when you don’t know in which object or field the data resides and you want to:
      * Retrieve data for a specific term that you know exists within a field. Because SOSL can tokenize multiple terms                     within a field and build a search index from this, SOSL searches are faster and can return more relevant results.
      * Retrieve multiple objects and fields efficiently, and the objects might or might not be related to one another.
      * Retrieve data for a particular division in an organization using the divisions feature, and you want to find it in the                      most efficient way possible.
```

*  Salesforce Federated Search allows you to make the global search box an external search engine. When Federated Search is set up, we transfer the user’s query to the external engine, which searches the external sources. The results are returned right in the Salesforce search results. We do this through the Salesforce Federated Search connector. The connector is built using the OpenSearch specification, so you can plug in any search engine that conforms to this industry standard.
