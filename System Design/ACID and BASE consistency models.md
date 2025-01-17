* Atomicity, Consistency, Isolation, and Durability
* ACID props are used for maintaining data integrity during transaction processing 
* ## Atomic 
	* All operations in transaction succeed or every operation is rolled back
* ## Consistent
	* Completion of transaction, database is structurally sound
* ##  Isolated 
	* Transactions don’t compete directly. The database manages conflicts, making them appear to run one at a time.
* ## Durable
	* Once the transaction has been completed and the writes and updates have been written to the disk, it will remain in the system even if a system failure occurs.

# Base
 
 * To increase the ability to scale and at the same time be highly available, we move the logic from the database to separate servers
 * database becomes more independent and focused on the actual process of storing data.
### Basic Availability
* Database appears to work most of the time
### Soft-state
* Stores don't have to be write-consistent, nor do different replicas have to be mutually consistent all the time
### Eventually consistency
* The data might not be consistent immediately but eventually, it becomes consistent.

# ACID vs BASE Trade-offs
Choosing between ACID and BASE depends on your application's needs. ACID ensures strict consistency, making it ideal for scenarios where data reliability is critical. BASE, with its loose consistency, offers scalability and availability but requires developers to handle data consistency carefully. While BASE suits distributed systems, its limitations can complicate development compared to the simplicity of ACID transactions.