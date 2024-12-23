 for searching a [[Trees]] and [[Graphs]]data structure for a node that satisfies a given property. It starts at the root and explores all nodes at the present depth prior to moving on to the nodes at the next depth level.
**Uses a Queue**

==Solving shortest Path problems== 

``` python
marked = | False | * G.size()
def bfs(G, root):
	queue = [v]
	while len(q) > 0:
		v = q.pop()
		if not marked|v|:
			visited(v)
			marked|v| = True
			for w in G.neighbors(v):
				if not marked|v|:
					q.append(v)
```