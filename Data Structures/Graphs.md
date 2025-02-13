---
tags:
  - 🌳Data-Structures
  - 🏷️Graphs
date: 2024-11-30T13:24
---
Far less restricted than trees (Very complicated!)
* No neighbor limit 
* Directed 
* Undirected 
* Cyclic
* Weighted edges 
## Notion 
G = (V,E)
V = nodes
E = edges

### Graph applications
![[grpah.png]]

# Graph Representations
* ### Adjacency matrix
	* n x n matrix
	* map each node if there is a 1 there is an edge otherwise no edge![[adjMat.png]]
	* #### Space: n^2
	* #### Checking if (u,v) is an edge takes O(1)
	* #### Identifying all edges takes O(n^2)
* ### Adjacency List
	* Node-indexed array of lists![[adjlist 1.png]]
	* #### Space: o(m +n)
	* #### Checking if (u,v) is an edge takes O(degree(u)), degree = number of neighbors of u 
	* #### Identifying all edges takes O(m +n)
* 
## Graph Traversal 
Algorithm to visit every node of a graph
* [[Depth First Search]]
* [[Breath First Search]]
* 