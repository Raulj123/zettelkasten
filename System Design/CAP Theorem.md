* CAP theorem states that a distributed system can deliver only two of the three desired characteristics Consistency, Availability, and Partition tolerance (CAP).
* [PARCELC Theorem](#PARCELC Theorem)
![[cap-theorem.webp]]
* ## Consistency
	*  All clients see the same data at the same time, no matter which node they connect to
	* Whenever data is written to one node, it must be instantly forwarded or replicated across all the nodes in the system before the write is deemed "successful"
* ## Availability
	* Availability means that any client making a request for data gets a response, even if one or more nodes are down.
* ## Partition Tolerance
	*  system continues to work despite message loss or partial failure

A ==**partition**== in a database means a break or failure in the network that prevents communication between some nodes in a distributed system.
# Consistency-Availability Tradeoff
We live in a physical world and can't guarantee the stability of a network, so ==distributed databases must choose Partition Tolerance (P).== This implies a tradeoff between Consistency (C) and Availability (A)

# CA (Consistency and Availability) Database
* A CA database delivers consistency and availability across all nodes. It can't do this if there is a partition between any two nodes in the system, and therefore can't deliver fault tolerance.
* Examples/ PostgreSQL, MariaDB

# CP (Consistency and Partition Tolerance) Database
* A CP database delivers consistency and partition tolerance at the expense of availability. When a partition occurs between any two nodes, the system has to shut down the non-consistent node until the partition is resolved.
* Examples/ MongoDB, Apache HBase

# AP(Availability and  Partition Tolerance) Database
* An AP database delivers availability and partition tolerance at the expense of consistency. When a partition occurs, all nodes remain available but those at the wrong end of a partition might return an older version of data than others. When the partition is resolved, the AP databases typically re-syncs the nodes to repair all inconsistencies in the system.
* Example/ Apache, Cassandra, CouchDB

# PARCELC Theorem
* The CAP theorem states that in the case of network partitioning (P) in a distributed system, one has to choose between Availability (A) and Consistency (C).
* PACELC extends the CAP theorem by introducing latency (L) as an additional attribute of a distributed system. The theorem states that ==else (E), even when the system is running normally in the absence of partitions, one has to choose between latency (L) and consistency (C).==
* PACELC theorem was developed to address a key limitation of the CAP theorem as it makes no provision for performance or latency.****
