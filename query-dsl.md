 Elasticsearch provides a full Query DSL \(Domain Specific Language\) based on JSON to define queries. Think of the Query DSL as an AST \(Abstract Syntax Tree\) of queries, consisting of two types of clauses:

**Leaf query clauses**

 Leaf query clauses look for a particular value in a particular field, such as the [`match`](https://www.elastic.co/guide/en/elasticsearch/reference/current/query-dsl-match-query.html), [`term`](https://www.elastic.co/guide/en/elasticsearch/reference/current/query-dsl-term-query.html) or [`range`](https://www.elastic.co/guide/en/elasticsearch/reference/current/query-dsl-range-query.html)

 queries. These queries can be used by themselves.

**Compound query clauses**

 Compound query clauses wrap other leaf **or ** compound queries and are used to combine multiple queries in a logical fashion \(such as the [`bool`](https://www.elastic.co/guide/en/elasticsearch/reference/current/query-dsl-bool-query.html) or [`dis_max`](https://www.elastic.co/guide/en/elasticsearch/reference/current/query-dsl-dis-max-query.html) query\), or to alter their behaviour \(such as the [`constant_score`](https://www.elastic.co/guide/en/elasticsearch/reference/current/query-dsl-constant-score-query.html) query\).

Query clauses behave differently depending on whether they are used in [query context or filter context](https://www.elastic.co/guide/en/elasticsearch/reference/current/query-filter-context.html).

