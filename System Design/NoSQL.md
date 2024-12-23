NoSQL databases are like a more ==flexible way to store data compared to traditional databases that use tables and strict rules (like Excel)==. Instead of needing a set structure, like rows and columns, NoSQL lets you save data in a more free-form way, like a messy notebook where each page can look different.

# Types 

### Document 
A document database stores data in "documents," like digital folders, instead of rows and tables. It's flexible, easy to scale, and doesn’t need a fixed structure.

**Pros:** Flexible, scalable, no strict structure.  
**Cons:** No strict structure, not relational.

**Examples:** MongoDB, Amazon DocumentDB, CouchDB.

### Key-value
A key-value database is like a big dictionary, storing data as pairs: a "key" (like a word) and its "value" (like the meaning).

**Pros:** Simple, fast, scalable, great for quick lookups.  
**Cons:** Limited features, no filtering or complex searches.

**Examples:** Redis, Memcached, Amazon DynamoDB, Aerospike.

### Graph
A graph database stores data as nodes and edges like a web of relationships instead of tables or documents.

**Pros:** Fast queries, flexible, shows relationships clearly.  
**Cons:** Complex, no standard query language.

**Uses:** Fraud detection, recommendations, social networks, network mapping.  
**Examples:** Neo4j, ArangoDB, Amazon Neptune, JanusGraph.
### Time series 
A time-series database is a database optimized for time-stamped, or time series, data.

**Pros**: Fast insertion and retrieval, Efficient data storage
**Uses**: IoT data, Metrics analysis, Application monitoring, Understand financial trends
**Examples**: InfluxDB, Apache Druid
### Wide Column
Wide column databases, also known as wide column stores, are schema-agnostic. Data is stored in column families, rather than in rows and columns.

**Pros:** Highly scalable, can handle petabytes of data, Ideal for real-time big data applications
**Cons**: Expensive, Increased write time
**Uses:** Business analytics, Attribute-based data storage
**examples**: BigTavle, Apache Cassandra. ScyllaDB
### Multi-Model
Multi-model databases combine different database models (i.e. relational, graph, key-value, document, etc.) into a single, integrated backend. This means they can accommodate various data types, indexes, queries, and store data in more than one model.

**Pros:** Flexibility, Suitable for complex projects, Data consistent
**Cons:** Complex, Less mature
**Examples:** ArangoDB, Azure Cosmos DB, Couchbase