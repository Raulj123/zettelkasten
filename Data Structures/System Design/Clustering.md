At a high level, a computer cluster is a group of two or more computers, or nodes, that run in parallel to achieve a common goal.
* allows workloads consisting of a high number of individual, parallelizable tasks to be distributed among the nodes in the cluster
* tasks can leverage the combined memory and processing power of each computer to increase overall performance.
* Typically, at least one node is designated as the leader node and acts as the entry point to the cluster
# Types
- **Highly Available (HA)**: Keeps services running even during failures.
- **Load Balancing**: Distributes workloads evenly across nodes.
- **High-Performance Computing (HPC)**: Solves heavy computational problems by splitting tasks.
# Configurations
- **For HA Clusters**:
    1. **Active-Active**: All nodes are active and share the workload.
    2. **Active-Passive**: One node is active; the passive node takes over if the active one fails.
- **For Load Balancing**: All nodes are typically active, distributing requests.
- **For HPC**: Nodes work in parallel to process different parts of a task