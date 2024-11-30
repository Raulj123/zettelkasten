---
tags:
  - 🌳Data-Structures
  - 🏷️stack-queues
date: 2024-11-30T13:10
---

# Stacks
Last in, first out (LIFO)
Can be done with array 
``` python
stack = []
stack.append('hi)
stack.pop()
```
# Time Complicity
All from the top 
* Push -> O(1)
* Pop -> O(1)
* Peek -> O(1)

# Queues
First in, First out (FIFO)
Done using array but not really cause:
> [!info]
Deque is preferred over list in the cases where we need quicker append and pop operations from both the ends of container, as deque provides an O(1) time complexity for append and pop operations as compared to list which provides O(n) time complexity. Instead of enqueue and deque, append() and popleft() functions are used.

### How its done
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
