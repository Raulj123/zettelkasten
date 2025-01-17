* A transaction is a series of database operations that are considered to be a _"single unit of work"_.
* _Usually, relational databases support ACID transactions, and non-relational databases don't (there are exceptions)._
* ![[transaction-states.webp]]
* ## Active 
	* Transaction is being executed, initial state of every transaction 
* ## Partially Committed 
	* Transaction executed final operation, said to be in a partially committed state 
* ## Committed 
	* If a transaction executes all its operations successfully, it is said to be committed. All its effects are now permanently established on the database system.
* ## Failed 
	* The transaction is said to be in a failed state if any of the checks made by the database recovery system fails. A failed transaction can no longer proceed further.
* ## Aborted 
	* Transaction reached failed state, rolls back all its write operations to bring DB back to the OG state 
	* Recovery module can select one of the two after a transaction aborts:
		* Restart the Transaction
		* Kill the transaction 
* ## Terminated 
	* If there isn't any roll-back or the transaction comes from the _committed state_, then the system is consistent and ready for a new transaction and the old transaction is terminated.