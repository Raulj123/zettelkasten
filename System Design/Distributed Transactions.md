* A distributed transaction is a ==set of operations on data that is performed across two or more databases.==
* It is typically coordinated across separate nodes connected by a network, but may also span multiple databases on a single server.

# Why do we need it?
A distributed transaction changes data in **multiple databases** at once.
It’s harder than a regular (ACID) transaction because all databases (nodes) must work together to make sure:
- **Everything succeeds** (all commit), OR
- **Everything fails** (all rollback).
This ensures consistency, so no system is left in a bad state.

# Two-Phase commit
* The two-phase commit (2PC) protocol is a distributed algorithm that coordinates all the processes that participate in a distributed transaction on whether to commit or abort (roll back) the transaction.
* achieves its goal even in many cases of temporary system failure and is thus widely used
* rare cases, manual intervention is needed to remedy an outcome.
*  requires a coordinator node, which basically coordinates and oversees the transaction across different nodes
* ## Phases
	* ## Prepare Phase
		* coordinator node collecting consensus from each of the participant nodes. The transaction will be aborted unless each of the nodes responds that they're _prepared_
	* ## Commit Phase
		*  all participants respond to the coordinator that they are _prepared_, then the coordinator asks all the nodes to commit the transaction. If a failure occurs, the transaction will be rolled back.
## Problems 
* What if one node crashes?
* what if coordinator crashes 
* It is a blocking protocol

# Three-Phase commit
* Three-phase commit (3PC) is an extension of the two-phase commit where the commit phase is split into two phases. This helps with the blocking problem that occurs in the two-phase commit protocol.
* ## Phases
	* ## Prepare phase
		* same as 2PC
	* ## Pre-commit phase
		* Coordinator issues the pre-commit message and all the participating nodes must acknowledge it. If a participant fails to receive this message in time, then the transaction is aborted.
	* ## Commit Phase
		* same as 2PC
# Why is the Pre-Commit phase helpful?
- If the participant nodes are found in this phase, that means that _every_ participant has completed the first phase. The completion of prepare phase is guaranteed.
- Every phase can now time out and avoid indefinite waits.

# Sagas
* A saga is a sequence of local transactions.
* Each local transaction updated the DB and publishes a message to the next local in the saga
* One fails then a series of a transaction undo the changes that were made

# Coordination
* ## Choreography 
	* Each service **acts on its own** and tells others what happened by sending events.
	- Example: Service A completes → sends "Done!" → triggers Service B.
* ## Orchestration 
	* A **central controller** (orchestrator) tells each service what to do and when.
	* Example: Orchestrator: "Service A, go!"