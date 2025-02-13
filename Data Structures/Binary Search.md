## When to use?
* Input is sorted and you need to find a number
* Finding the position of insertion in a sorted list
* Handling duplicates in sorted arrays
* Searching in rotated sorted arrays
### Technique 
u know this b tf, left ptr set to 0 and right to end of array, find the midpoint check if target if greater move right down one and vice versa.

```python
l, r = 0, len(nums) -1

while l <= r:
	m = l + r // 2
	if nums[m] == target:
		return m
	if nums[m] > target:
		r = m - 1
	else:
		l = mid + 1
return - 1
```


| Medium | [Find First and Last Position of Element in Sorted Array](https://leetcode.com/problems/find-first-and-last-position-of-element-in-sorted-array/) | This is tricky two searches one for right and left side |
| ------ | ------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------- |
| Medium | [Find Minimum in Rotated Sorted Array](https://leetcode.com/problems/find-minimum-in-rotated-sorted-array/)                                       | find pivot point, change pointers if less or greater    |
|        |                                                                                                                                                   |                                                         |
