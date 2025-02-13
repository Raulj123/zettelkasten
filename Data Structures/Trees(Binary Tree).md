---
tags:
  - 🌳Data-Structures
  - 🏷️trees
date: 2024-11-30T13:12
---
Binary tree is just one many more 

* Nodes connected via edges
* Root node (first node)
* Parent -> child 
* leave nodes (no children)

# Binary Tree
Where each parent node has at most two children 

# Binary Search Tree
* All nodes on left are less than the parent node
* All nodes on the right are greater then the parent node

# Time Complexity 
Binary search *o(logn)*
Only works if list is sorted! 
## How to

``` python
nums = [1,2,3,4,5........98,99,100]
l, r = 0, len(nums) - 1

while l <= r:
	m = r + l // 2
	if nums[m] > target:
		r = m - 1
	elif nums[m] < target:
		l = m + 1
	else:
		return nums[m]
```

## Types of Binary Trees
* A **complete** binary tree is a binary tree in which every level, _except possibly the last_, is completely filled, and all nodes in the last level are as far left as possible.
* Example![[Pasted image 20250129103902.png]]
