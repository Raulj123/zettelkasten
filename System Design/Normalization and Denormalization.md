[Video that helped a lot](https://www.youtube.com/watch?v=GFQaEYEc8_8)

# Terms
**Primary key**: Column or group of columns that can be used to uniquely identify every row of the table.

**Composite key**: A primary key made up of multiple columns.

**Super key**: Set of all keys that can uniquely identify all the rows present in a table.

**Candidate key**: Attributes that identify rows uniquely in a table.

**Foreign key**: It is a reference to a primary key of another table.

**Alternate key**: Keys that are not primary keys are known as alternate keys.

**Surrogate key**: A system-generated value that uniquely identifies each entry in a table when no other column was able to hold properties of a primary key.

# Dependencies
* ***Partial dependency**: Occurs when the primary key determines some other attributes.

* ***Functional dependency**: It is a relationship that exists between two attributes, typically between the primary key and non-key attribute within a table.

* ***Transitive functional dependency**: Occurs when some non-key attribute determines some other attribute.

# Anomalies
Database anomaly happens when there is a flaw in the database due to incorrect planning or storing everything in a flat database.

*  ***Insertion anomaly**: Occurs when we are not able to insert certain attributes in the database without the presence of other attributes.

* ***Update anomaly**: Occurs in case of data redundancy and partial update. In other words, a correct update of the database needs other actions such as addition, deletion, or both.

* ***Deletion anomaly**: Occurs where deletion of some data requires deletion of other data.

# Normalization
Normalization is the process of organizing data in a database. This includes creating tables and establishing relationships between those tables according to rules designed both to protect the data and to make the database more flexible by eliminating redundancy and inconsistent dependency.

* ### Why do we need it?
	* eliminate redundant data and ensure data is consistent
* ### Normal Forms
	 * series of guidelines to ensure that the database is normalized
	 * #### 1NF
		 * For a table to be in this form should follow the following rules:
		 * Repeating groups are not permitted.
		 * Identify each set of related data with a primary key.
		- Set of related data should have a separate table.
		- Mixing data types in the same column is not permitted.
	* #### 2NF
		* Satisfies the first normal form (1NF).
		- Should not have any partial dependency.
	* #### 3NF
		* Satisfies the second normal form (2NF).
		- Transitive functional dependencies are not permitted.
	* #### BNCNF
		* Boyce-Codd normal form (or BCNF) is a slightly stronger version of the third normal form (3NF) used to address certain types of anomalies not dealt with by 3NF as originally defined. Sometimes it is also known as the 3.5 normal form (3.5NF).
		* Satisfied the third normal form (3NF).
		- For every functional dependency X → Y, X should be the super key.- Satisfied the third normal form (3NF).

For every functional dependency X → Y, X should be the super key.
### Advantages 
* Reduces data redundancy.
- Better data design.
- Increases data consistency.
- Enforces referential integrity.
### Disadvantages 
* Data design is complex.
- Slower performance.
- Maintenance overhead.
- Require more joins.

# Denormalization 
Database optimization technique in which we add redundant data to one or more tables. This can help us avoid costly joins in a relational database. It attempts to improve read performance at the expense of some write performance. Redundant copies of the data are written in multiple tables to avoid expensive joins.

### Advantages
- Retrieving data is faster.
- Writing queries is easier.
- Reduction in number of tables.
- Convenient to manage.

### Disadvantages
- Expensive inserts and updates.
- Increases complexity of database design.
- Increases data redundancy.
- More chances of data inconsistency.