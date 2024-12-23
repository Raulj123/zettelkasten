# What is a Database?
* Organized collection of structured information, or data typically stored electronically in a computer system. 
*  ==Database is usually controlled by a Database Management System (DBMS).== 
* Together, the data and the DBMS, along with the applications that are associated with them, are referred to as a database system, often shortened to just database.
# What is a DBMS
* A DBMS serves as an ==interface between the database and its end-users or programs, allowing users to retrieve, update,== and manage how the information is organized and optimized.
* facilitates oversight and control of databases, enabling a variety of administrative operations such as performance monitoring, tuning, and backup and recovery.
# Components 
Found across different databases 
* ### Schema
	* A schema defines the structure and rules for organizing data. It can be:
		* Strictly Enforced: All data must follow the schema, typical in relational databases (e.g., SQL).
		 * Loosely Enforced: Only some parts must follow the schema, common in semi-structured data (e.g., JSON).
		 * Schema-less: No predefined structure, typical in NoSQL databases (e.g., MongoDB).
* ### Table 
	* Each table contains various columns just like in a spreadsheet. A table can have as meager as two columns and upwards of a hundred or more columns
* ### Column
	* A column contains a set of data values of a particular type, one value for each row of the database.
* ### Row
	* Data in a table is recorded in rows. There can be thousands or millions of rows in a table having any particular information.
# Types
- [[SQL]]
- [[NoSQL]]
    - Document
    - Key-value
    - Graph
    - Timeseries
    - Wide column
    - Multi-model