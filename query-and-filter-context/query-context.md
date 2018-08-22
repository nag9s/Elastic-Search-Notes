 Query context is in effect whenever a query clause is passed to a `query ` parameter, such as the `query ` parameter in the [`search`](https://www.elastic.co/guide/en/elasticsearch/reference/current/search-request-query.html) API.



 A query clause used in query context answers the question “_How well does this document match this query clause? _” Besides deciding whether or not the document matches, the query clause also calculates a `_score` representing how well the document matches, relative to other documents.

