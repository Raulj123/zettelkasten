---
tags:
  - 🌳Data-Structures
  - 🏷️stack-queues
date: 2024-11-30T13:10
---
What are they good for? 
* Tree data structure
* DFS for stack
* BFS for queue
# Stacks
Last in, first out (LIFO)
* Implemented either through an array or linked list(all it is a specials list) 
* What identifies the data structure as a stack is not the implementation but the **interface
* User is only allowed to pop or push items
* Some languages, such as [Perl](https://en.wikipedia.org/wiki/Perl "Perl"), [LISP](https://en.wikipedia.org/wiki/Lisp_(programming_language) "Lisp (programming language)"), [JavaScript](https://en.wikipedia.org/wiki/JavaScript "JavaScript") and [Python](https://en.wikipedia.org/wiki/Python_(programming_language) "Python (programming language)"), make the stack operations push and pop available on their standard list/array types.
*  [[Depth First Search]]
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
* The operation of adding an element to the rear of the queue is known as _enqueue_, and the operation of removing an element from the front is known as _dequeue_. Other operations may also be allowed, often including a _[peek](https://en.wikipedia.org/wiki/Peek_(data_type_operation) "Peek (data type operation)")_ or _front_ operation that returns the value of the next element to be dequeued without dequeuing it.
* First in, First out (FIFO)
* [[Breath First Search]]
* Done using array but not really cause:
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
