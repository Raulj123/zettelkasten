* architectural pattern that divides a system's actions into commands and queries
* command is an instruction, a directive to perform a specific task
* _query_ is a request for information that doesn't change the system's state or cause any side effects
* CQRS pattern is often used along with [[Event Sourcing]]
* When used with the Event Sourcing pattern, the store of events is the write model and is the official source of information
* Advantages 
	- Allows independent scaling of read and write workloads.
	- Easier scaling, optimizations, and architectural changes.
	- Closer to business logic with loose coupling.
	- The application can avoid complex joins when querying.
	- Clear boundaries between the system behavior.
* Disadvantages
	- More complex application design.
	- Message failures or duplicate messages can occur.
	- Dealing with eventual consistency is a challenge.
	- Increased system maintenance efforts.
	