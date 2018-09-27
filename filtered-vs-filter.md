[https://stackoverflow.com/questions/38744489/filtered-bool-vs-bool-query-elasticsearch](https://stackoverflow.com/questions/38744489/filtered-bool-vs-bool-query-elasticsearch)

[https://www.elastic.co/guide/en/elasticsearch/reference/current/query-dsl-filtered-query.html](https://www.elastic.co/guide/en/elasticsearch/reference/current/query-dsl-filtered-query.html)

[`filtered`](https://www.elastic.co/guide/en/elasticsearch/reference/current/query-dsl-filtered-query.html) \(Old 1.x Syntax\) queries have been deprecated in favor of [`bool/filter`](https://www.elastic.co/guide/en/elasticsearch/reference/current/query-dsl-bool-query.html)



Mastering Elasticsearch 5.x

with the release of Lucene 5.0, which is used by

Elasticsearch version 2.0.0, both queries and filters became the same

internal object, taking care of both document relevance and matching.

So, an Elasticsearch query that used to look like the following

{"

filtered" : {

"query": { query definition },

"filter": { filter definition }

}

}

It should now be written like this in version 2.x:

{"

bool" : {

"must": { query definition },

"filter": { filter definition }

}}

