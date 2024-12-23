A SQL ==(or relational) database is a collection of data items with pre-defined relationships between them.== These items are organized as a set of tables with columns and rows. ==Tables are used to hold information about the objects to be represented in the database.== Each column in a table holds a certain kind of data and a field stores the actual value of an attribute. The rows in the table represent a collection of related values of one object or entity.

==Each row in a table could be marked with a unique identifier called a primary key,== and rows among multiple tables can be made related using ==foreign keys==. This data can be accessed in many different ways without re-organizing the database tables themselves. SQL databases usually follow the [ACID consistency model]

# Materialized Views
A materialized view is a ==pre-computed data set derived from a query specification and stored for later use.== Because the data is pre-computed, ==querying a materialized view is faster than executing a query against the base table of the view==. This performance difference can be significant when a query is run frequently or is sufficiently complex.

# N+1 query problem 
The N+1 query problem happens when the data access layer executes N additional SQL statements to fetch the same data that could have been retrieved when executing the primary SQL query.

# ORM(Object-Relation Mapping)
translator between your code and your database. It lets you use objects and classes in your programming language (like Python, Java, or JavaScript) instead of writing raw SQL queries to talk to the database.

# Advantages
* Simple and accurate
- Accessibility
- Data consistency
- Flexibility
# Disadvantages
- Expensive to maintain
- Difficult schema evolution
- Performance hits (join, denormalization, etc.)
- Difficult to scale due to poor horizontal scalability

# Commonly used relation DB
* PostgreSQL
* MySQL
* MariaDB
* Amazon Aurora