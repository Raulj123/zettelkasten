## When to use it?
* Linear data structures (arrays, lists, strings)
* Detect cycle in linked list
* Find middle of linked list
* Perform in one pass with O(1) space

## Technique 
* Use two pointers, a slow and fast pointer
* Slow moves once and fast moves twice at every iteration
* ## What can you find?
	* if fast == slow there is a cycle
	* if found cycle and reset slow and loop again till they meet you found start of cycle, there is a proof for this forgot what its called
	* Find second half of a linked list
* ### Dummy node?
	* if modify the head of the list best to use this 

### Template
```python
fast = head
slow = head

while fast and fast.next:
	fast = fast.next.next
	slow = slow.next

	if fast == slow:
		# cycle 
return False
```


| Difficulty | Link                                                                                                |                                              |
| ---------- | --------------------------------------------------------------------------------------------------- | -------------------------------------------- |
| Easy       | [Linked List Cycle](https://leetcode.com/problems/linked-list-cycle/)                               |                                              |
| Medium     | [Linked List Cycle II](https://leetcode.com/problems/linked-list-cycle-ii/)                         |                                              |
| Medium     | [Remove Nth Node From End of List](https://leetcode.com/problems/remove-nth-node-from-end-of-list/) | Used a dummy node                            |
| Easy       | [Reverse Linked List](https://leetcode.com/problems/reverse-linked-list/)                           | lots of placeholders and temps and switching |
| Medium     | [Reorder List](https://leetcode.com/problems/reorder-list/)                                         | find in half, reverse second half, and merge |
| Medium     | [Reverse Linked List II](https://leetcode.com/problems/reverse-linked-list-ii/)                     | I cant do this one b                         |
|            |                                                                                                     |                                              |
