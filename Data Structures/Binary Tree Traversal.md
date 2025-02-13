* Binary tree - each node has at most **two children** (left and right).
* Binary Search Tree(BST) - left nodes are **smaller** and right nodes are **greater** than the parent.
## When to use?
* Preorder: Serialize or deserialize a tree
* Inorder: Retrieve elements in sorted order (BSTs)
* Postorder: Process children before parent (bottom-up)
* [[Breath First Search]]: Level by level scanning
	``` python
from collections import deque
q = deque()
q.append("hi)
q.popleft()
```
# Time Complexity
* Enqueue -> O(1)  removed from the back of queue
* Dequeue -> O(1) removed form the front of queue
* Front -> O(1)  peek at the front of queue



> [!IMORTANT] For preorder, inorder, and postorder use recursion (DFS)

### Preorder (Root, L, R)
Pre-order traversal is to visit the root first. Then traverse the left subtree. Finally, traverse the right subtree.
```python
def PreOrder(node):
	if not node:
		return
	# VISIT NODE
	PreOrder(node.left)
	PreOrder(node.right)
```

### Inorder (L, Root, R)
* In-order traversal is to traverse the left subtree first. Then visit the root. Finally, traverse the right subtree.
* Typically, for `binary search tree`, we can retrieve all the data in sorted order using in-order traversal
```python
def InOrder(node):
	if not node:
		return
	PreOrder(node.left)
	# VISIT NODE
	PreOrder(node.right)
```

### Postorder
Post-order traversal is to traverse the left subtree first. Then traverse the right subtree. Finally, visit the root.
```python
def PostOrder(node):
	if not node:
		return
	PreOrder(node.left)
	PreOrder(node.right)
	# VISIT NODE
```


| Difficulty | Link                                                                                                  |                                                             |
| ---------- | ----------------------------------------------------------------------------------------------------- | ----------------------------------------------------------- |
| Easy       | [Maximum Depth of Binary Tree](https://leetcode.com/problems/maximum-depth-of-binary-tree/)           | Hard part is figuring out how to count a level max(l,r) + 1 |
| Medium     | [Binary Tree Level Order Traversal](https://leetcode.com/problems/binary-tree-level-order-traversal/) | BFS                                                         |
| hard       | [Binary Tree Maximum Path Sum](https://leetcode.com/problems/binary-tree-maximum-path-sum/)           | postorder                                                   |
|            |                                                                                                       |                                                             |
