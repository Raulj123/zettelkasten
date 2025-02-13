* [[Trees]] based data structure that satisfies a heap property
* Max heap - any given node C with parent node P then value is greater or equal to C
* Min heap - any given node C with parent node P then value is less than or equal to C
* In a heap the highest or lowest priority element is always stored at the root
* **Not sorted, regarded as partially ordered** 
* A complete binary tree - every level, _except possibly the last_, is completely filled, and all nodes in the last level are as far left as possible

# Operations
in python heapq module allows us to treat a list as a heap(usually implemented as min heaps)
```python
import heapq

heapq.heapify(list)           #rearranges list into a valid heap 
heapq.heappush(list,5)        # appending an element
minEl = heapq.heappop(list)  #pops smallest element 0(logN) n in heap
heap.heappushpop(list,5)      #push new element and pop smallest at same time

max = heapq.nlargest(3,list)  #largest 3 elements
min = heapq.nsmallest(3,list) #smallest 3 elements

```

#### Storing tuples with heaps
When you use heapq with a tuple in Python, it uses the first element of the tuple as the primary key for sorting and maintaining the heap order. If multiple tuples have the same first element, it will use the second element, then the third, and so on, to break ties.

in case u forgot range(start, stop, step)


| Difficulty | Link                                                                                              |                                                                                                                                                                                                                                                                                                                                                                                                             |
| ---------- | ------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Medium     | [Kth Largest Element in an Array](https://leetcode.com/problems/kth-largest-element-in-an-array/) | min heap of size k, smallest on top will be popped off, will be left with k largest in list so pop of min                                                                                                                                                                                                                                                                                                   |
| Medium     | [Top K Frequent Elements](https://leetcode.com/problems/top-k-frequent-elements/)                 | o(nlogK)<br>sol 1: use a freq, use a min heap to storer as tuple, if goes over pop the tuple,  at end will be left of tuples with k largest freq<br><br>o(n)<br>sol2: if len is n no way that an num will appear more than n times, so we use an array of len n + 1(to count for 0) to store the index as freq and num as the element, iterate the array backwards and do that until len of the result is k |
| Hard       | [Merge k Sorted Lists](https://leetcode.com/problems/merge-k-sorted-lists/)                       |                                                                                                                                                                                                                                                                                                                                                                                                             |
|            |                                                                                                   |                                                                                                                                                                                                                                                                                                                                                                                                             |
|            |                                                                                                   |                                                                                                                                                                                                                                                                                                                                                                                                             |
