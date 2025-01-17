
 1) Clarify requirements
	 *  ==Divided into three parts==
		 1)  ==Functional requirements==
			 *  requirements that the end user specifically demands as basic functionalities that the system should offer
			 *  Example:
				 - "What are the features that we need to design for this system?"
				*  "What are the edge cases we need to consider, if any, in our design?"
		2) ==Non-functional requirements== 
			* quality constraints that the system must satisfy according to the project contract
			* Example:
				- "Each request should be processed with the minimum latency"
				*  "System should be highly available"
		3) Extended Requirements 
			* "nice to have" requirements 
			* Example
				- "Our system should record metrics and analytics"
				- "Service health and performance monitoring?"
 2) ==Estimation and Constraints==
    * "What is the desired scale that this system will need to handle?"
	- "What is the read/write ratio of our system?"
	- "How many requests per second?"
	- "How much storage will be needed?"
3) ==Data model design==
	*  start with defining the database schema
	* Examples
		* "What are the different entities in the system?"
		- "What are the relationships between these entities?"
		- "How many tables do we need?"
		- "Is NoSQL a better choice here?"
4) ==API design==
	* simple interface defining the API requirements such as parameters, functions, classes, types, entities, etc.
```python
createUser(name: string, email: string): User

```
5) ==High-level component Design==
	* identify system components (such as Load Balancers, API Gateway, etc.) that are needed to solve our problem and draft the first design of our system.
	- "Is it best to design a monolithic or a microservices architecture?"
	- "What type of database should we use?"
6) ==Detailed design==
	* go into detail about the major components of the system we designed.
	* Examples
		* "How should we partition our data?"
		- "What about load distribution?"
		- "Should we use cache?"
		- "How will we handle a sudden spike in traffic?"
7) Identify and resolve bottlenecks
	* "Do we have enough database replicas?"
	- "Is there any single point of failure?"
	- "Is database sharding required?"
	- "How can we make our system more robust?"
	- "How to improve the availability of our cache?"