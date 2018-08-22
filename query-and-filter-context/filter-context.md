 **Filter context is in effect whenever a query clause is passed to **a `filter` parameter, such as the `filter` or `must_not`parameters in the [`bool`](https://www.elastic.co/guide/en/elasticsearch/reference/current/query-dsl-bool-query.html) query, the `filter` parameter in the [`constant_score`](https://www.elastic.co/guide/en/elasticsearch/reference/current/query-dsl-constant-score-query.html) query, or the [`filter`](https://www.elastic.co/guide/en/elasticsearch/reference/current/search-aggregations-bucket-filter-aggregation.html) aggregation.



In _filter_ context, a query clause answers the question “_Does this document match this query clause?_” The answer is a simple Yes or No — no scores are calculated. Filter context is mostly used for filtering structured data, e.g.

* _Does this `timestamp` fall into the range 2015 to 2016?_
* _Is the `status` field set to `"published"`_?

Frequently used filters will be cached automatically by Elasticsearch, to speed up performance.

