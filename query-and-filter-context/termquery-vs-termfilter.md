https://discuss.elastic.co/t/termquery-vs-termfilter/4839

Which query should I prefer? This filter query:

srb.setQuery\(QueryBuilders.filteredQuery\(QueryBuilders.matchAllQuery\(\),  
 FilterBuilders.termFilter\("someField", "someValue"\)\)\);

or this termQuery:

srb.setQuery\(QueryBuilders.termQuery\("someField", "someValue"\)\);



** Use a term query if the terms you are looking for should affect the  \_score \(relevance\). If it should just exclude all docs except for those  that match, use a term filter.**





https://www.elastic.co/guide/en/elasticsearch/guide/current/\_queries\_and\_filters.html



**Historically, queries and filters were separate components in Elasticsearch. Starting in Elasticsearch 2.0, filters were technically eliminated, and all queries gained the ability to become non-scoring.**

**However, for clarity and simplicity, we will use the term "filter" to mean a query which is used in a non-scoring, filtering context. You can think of the terms "filter", "filtering query" and "non-scoring query" as being identical.**

**Similarly, if the term "query" is used in isolation without a qualifier, we are referring to a "scoring query".**

