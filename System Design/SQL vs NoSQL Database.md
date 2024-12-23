In the world of databases, there are two main types of solutions, SQL (relational) and NoSQL (non-relational) databases. Both of them differ in the way they were built, the kind of information they store, and how they store it. ==Relational databases are structured and have predefined schemas while non-relational databases are unstructured, distributed, and have a dynamic schema.==

# High-level differences 

## Storage 
* SQL- Stores data in tables, each row is entity and each col is a data point about that entity
* NoSQL- different data storage models, key-value, graph, doc etc.
## Schema 
* SQL- each record conforms to a fixed schema cols must be decided and chosen before data entry and each row must have data for each col, can be altered later but requires **database migrations**
* NoSQL- schemas are dynamic, each record doesn't have to contain data for each field
## Querying 
* SQL- db using SQL use SQL lol
* NoSQL- queries are focused on a collection of documents, different db use different syntax
## Scalability
* SQL- In most common situations, SQL databases are vertically scalable, which can get very expensive. It is possible to scale a relational database across multiple servers, but this is a challenging and time-consuming process.
* NoSQL-  horizontally scalable, meaning we can add more servers easily to our NoSQL database infrastructure to handle large traffic. Any cheap commodity hardware or cloud instances can host NoSQL databases, thus making it a lot more cost-effective than vertical scaling. A lot of NoSQL technologies also distribute data across servers automatically.
## Reliability
* SQL- The vast majority of relational databases are ACID compliant. So, when it comes to data reliability and a safe guarantee of performing transactions, SQL databases are still the better bet.
* NoSQL- Most of the NoSQL solutions sacrifice ACID compliance for performance and scalability.

**For SQL**
- Structured data with strict schema
- Relational data
- Need for complex joins
- Transactions
- Lookups by index are very fast

**For NoSQL**
- Dynamic or flexible schema
- Non-relational data
- No need for complex joins
- Very data-intensive workload
- Very high throughput for IOPS