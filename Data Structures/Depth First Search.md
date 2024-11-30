---
tags:
  - 🌳Algo
  - 🏷️DFS
date: 2024-11-30T13:34
---
Between which node to explore must be clear on how to make these choices on problem

## Recursive 
Have not done it this way (Cleaner and easier to read)
``` python
marked = [false] * G.size()
def dfs(G, node):
	v.append(node)
	marked[node] = True
	for v in G.neighbors(node):
		if not marked[v]:
			dfs(G, v)
```

## Iterative 
Uses a Stack [[Stacks and Queues]] (More generalizable)
``` python
marked = [false] * G.size()
def dfs(G, node):
	stack = [node]
	while len(stack) > 0:
		v = stack.pop()
		if not maked[v]:
			vist(v)
			marked[v] = True
			for w in G.neighbors(node):
				if not marked[w]:
					stack.append(w)
```

# Time Complexity 
Both run un O(V + E)

# Preorder
Out the vertex as a part of the order as soon as we encounter a new vertex 

# Post order 
Only after there is no where to explore for that vertex 
``` python
marked = [false] * G.size()
def dfs(G, node):
	v.append(node)
	marked[node] = True
	for v in G.neighbors(node):
		if not marked[v]:
	# move this guys after it called back!
	dfs(G, v)
```
