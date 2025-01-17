A common way to distribute data among servers is **Simple Hashing**
* Each object hash its key
* Maps to a known range of numerical values 
* Modulo on hash against number of server(n)
* Always map to same servers if n stays the same if not lots of data being moved if on server gets added or removed 

Goal of consistent hashing is we want all objects to stay assigned to the same server even if n changes

* hash object keys like before, hash server names 
* Maps to a range of x0 - xn (hash space)
* connect both ends to form a ring (hash ring)
* map both servers and objects onto the hash ring using a uniformly distributed hash function 
* to locate a server for an object we go clockwise on the rings position until sever is found
* PROBLEM: not evenly spaced out,
	* SOLUTION: each server has 3 virtual nodes 

Used in: 
* Apache Cassandra 
* Amazon DynamoDB