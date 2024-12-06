---
tags:
  - 🌳Data-Structures
  - 🏷️stack-queues
date: 2024-11-30T13:10
---
What are they good for? 
* Tree data structure
* [[Depth First Search]]
* [[Breath First Search]]
# Stacks
Last in, first out (LIFO)
* Implemented either through an array or linked list(all it is a specials list) 
* What identifies the data structure as a stack is not the implementation but the **interface
* user is only allowed to pop or push items
* 
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
