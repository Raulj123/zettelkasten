 Data Partitioning -  break up a database into many smaller parts. It is the process of splitting up a database or a table across multiple machines to improve the manageability, performance, and availability of a database.
# Methods
Two methods to break up an apps DB into smaller DB's
* ## Horizontal Partitioning(sharding)
	* In this strategy, we split the table data horizontally based on the range of values defined by the _partition key_. It is also referred to as **_database sharding_**.
* ## Vertical Partitioning 
	* partition the data vertically based on columns. We divide tables into relatively smaller tables with few elements, and each part is present in a separate partition.

# What is sharding?
* practice of separating one table's rows into multiple different tables, known as _partitions_ or _shards_
* cheaper and more feasible to scale horizontally by adding more machines than to scale it vertically by adding powerful servers.

**methods** used to decide **how to divide the data** into smaller parts (partitions):
## Hash-Based
This strategy divides the rows into different partitions based on a hashing algorithm rather than grouping database rows based on continuous indexes.
The disadvantage of this method is that dynamically adding/removing database servers becomes expensive.

## List-Based
In list-based partitioning, each partition is defined and selected based on the list of values on a column rather than a set of contiguous ranges of values.

## Range Based
partition the table in such a way that each partition contains rows within a given range defined by the partition key.

## Composite
composite partitioning partitions the data based on two or more partitioning techniques. Here we first partition the data using one technique, and then each partition is further subdivided into sub-partitions using the same or some other method.

# Advantages
- **Availability**: Provides logical independence to the partitioned database, ensuring the high availability of our application. Here individual partitions can be managed independently.
- **Scalability**: Proves to increase scalability by distributing the data across multiple partitions.
- **Security**: Helps improve the system's security by storing sensitive and non-sensitive data in different partitions. This could provide better manageability and security to sensitive data.
- **Query Performance**: Improves the performance of the system. Instead of querying the whole database, now the system has to query only a smaller partition.
- **Data Manageability**: Divides tables and indexes into smaller and more manageable units.
# Disadvantages
- **Complexity**: Sharding increases the complexity of the system in general.
- **Joins across shards**: Once a database is partitioned and spread across multiple machines it is often not feasible to perform joins that span multiple database shards. Such joins will not be performance efficient since data has to be retrieved from multiple servers.
- **Rebalancing**: If the data distribution is not uniform or there is a lot of load on a single shard, in such cases, we have to rebalance our shards so that the requests are as equally distributed among the shards as possible.

# When to use Sharding 
- Leveraging existing hardware instead of high-end machines.
- Maintain data in distinct geographic regions.
- Quickly scale by adding more shards.
- Better performance as each machine is under less load.
- When more concurrent connections are required.