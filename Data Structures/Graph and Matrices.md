* ==**Binary Tree**:== A hierarchical data structure where each node has at most two children (left and right).
* ==Matrix:== A 2D array of elements arranged in rows and columns.
* ==Graph:== A network of nodes (vertices) connected by edges, which can be directed or undirected.

Review: [[Graphs]]
## When to use?
* Search graphs or matrices
* [[Depth First Search]]: Explore all possible paths (e.g., maze)
* [[Breath First Search]]: Find the shortest path
* Topological Sort: Order tasks based on dependencies


| Difficulty | Link                                                                                      |                                                                                                                                                                                                                              |
| ---------- | ----------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Medium     | [Word Search](https://leetcode.com/problems/word-search/)                                 | for each spot call dfs, if not outside bounds over or under and is a valid char and we have not seen it (in path) in the search then call dfs again                                                                          |
| Medium     | [Course Schedule](https://leetcode.com/problems/course-schedule/)                         | make an adj list to represent the graph, loop through n and call dfs, base case if have seen the node, once we done and found no cycle then remove node off set and set given node in list value to empty list since we knoe |
| Medium     | [Rotting Oranges](https://leetcode.com/problems/rotting-oranges/)                         | count fresh and append rotten in queue, loop through q for the whole length of q, go through each through directions and append to q only if in bounds and if fresh and turn that spot rotten                                |
| Medium     | [Pacific Atlantic Water Flow](https://leetcode.com/problems/pacific-atlantic-water-flow/) | so we  know each border can reach each ocean so call dfs on left and right border with different sets. and call recursive if its a valid cell and new, return union of both sets                                             |
| Medium     | [Number of Islands](https://leetcode.com/problems/number-of-islands/)                     | simple bfs                                                                                                                                                                                                                   |
| Medium     | [Max Area of Island](https://leetcode.com/problems/max-area-of-island/)                   | simple bfs again forgot the only call if its a island and count is as one already instead of setting as 0.                                                                                                                   |
|            |                                                                                           |                                                                                                                                                                                                                              |
