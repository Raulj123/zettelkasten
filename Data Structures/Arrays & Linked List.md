---
tags:
  - 🌳Data-Structures
  - 🏷️Array-linked-list
date: 2024-11-29T17:39
---
# Array
### Array vs List?
* Array has one type of values (int for example). 
* List you can put different types (int, string, etc.)
* list can be dynamically resized, whereas a classical array is static.
* In python the array module can be dynamic  but hold only 1 data type
[1,3,4,5] or [9, "hi", false]
* Ordered collection of data
* Find an element based on index
* Stored in contiguous memory(each element is next to one another in mem)

## Time Complexity 
- Read -> O(1)
- Insert -> O(n)
- Delete -> O(n)

# Linked List
() -> () -> () -> 
* Singly linked lists contain nodes which have a 'value' field as well as 'next' field, which points to the next node in line of nodes.
* Each element in list has a [[Pointer]] which has next address of next element 
* Do not have to be stored next to each other 
* Not index based 

## Time Complexity 
* Read -> O(n)
* Insert -> O(1)
* Delete -< O(1)

* In a 'doubly linked list', each node contains, besides the next-node link, a second link field pointing to the 'previous' node in the sequence. The two links may be called 'forward('s') and 'backwards', or 'next' and 'prev'('previous').
