## When to use it?
* Linear data structures (arrays, lists, strings)
* Must scan through a subarray or substring
* When the subarray must satisfy some condition (shortest/longest/min/max)
* Improve time complexity from O(N^2) to O(N)
* Finding length of window **(right - left) + 1** 
# Dynamic Sliding Window 
* In the dynamic sliding window, the size of the window (subarray between i and j) changes throughout the algorithm
* usually use a set to hold distinct characters  
* for loop for the right pointer usually 
* some sort of condition to meet in order to shrink window 

| Difficulty                   | Link                                                                                                                                         |
| ---------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------- |
| Medium                       | [Longest Substring Without Repeating Characters](https://leetcode.com/problems/longest-substring-without-repeating-characters/)              |
| Medium(harder than previous) | [Longest Repeating Character Replacement](https://leetcode.com/problems/longest-repeating-character-replacement/)                            |
| Medium                       | [1493. Longest Subarray of 1's After Deleting One Element](https://leetcode.com/problems/longest-subarray-of-1s-after-deleting-one-element/) |
``` python
result = None
l = 0
# some data structure to keep unique chars or w/e, set, map
sett = set()
freq = defaultdict(int)

for r in range(len(s)):
	# Expand Widnow add to sett or map
	while not condition():
		# remove from sett or map
		l += 1
	result = max(result, r - l + 1)	
	# Update the result if the current window is larger
    if r - l + 1 > max_length:
        max_length = r - l + 1
        # Add business logic to update result

```


# Fixed Sliding Window 
* size of the window is the same length throughout the algorithm

| Difficulty | Link                                                                                                                       |
| ---------- | -------------------------------------------------------------------------------------------------------------------------- |
| Easy       | [Substrings of Size Three with Distinct](https://leetcode.com/problems/substrings-of-size-three-with-distinct-characters/) |
| Medium     | [Maximum Points You Can Obtain from Cards](https://leetcode.com/problems/maximum-points-you-can-obtain-from-cards/)        |
