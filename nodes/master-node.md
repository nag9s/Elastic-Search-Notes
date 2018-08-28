

https://www.elastic.co/guide/en/elasticsearch/reference/5.4/modules-node.html

The master node is responsible for lightweight cluster-wide actions such as creating or deleting an index, tracking which nodes are part of the cluster, and deciding which shards to allocate to which nodes. It is important for cluster health to have a stable master node.

**Important  - ** While master nodes can also behave as [coordinating nodes](https://www.elastic.co/guide/en/elasticsearch/reference/5.4/modules-node.html#coordinating-node) and route search and indexing requests from clients to data nodes, it is better _not _ to use dedicated master nodes for this purpose. It is important for the stability of the cluster that master-eligible nodes do as little work as possible.

