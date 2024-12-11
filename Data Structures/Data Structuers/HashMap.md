---
tags:
  - 🌳Data-Structures
  - 🏷️Hash
date: 2024-11-30T12:56
---
{key: value}, Hash tables = Dictionaries 
* Key value pair 
* unordered 
* HashMap is created from an array through the use of a Hash function
*  A hash table uses a [hash function](https://en.wikipedia.org/wiki/Hash_function "Hash function") to compute an _index_, also called a _hash code_, into an array of _buckets_ or _slots_, from which the desired value can be found. During lookup, the key is hashed and the resulting hash indicates where the corresponding value is stored.
* Once hash function maps data to a key they can not change this key, key must be immutable(such as an array). You will get a type error 
* `defaultdict` == All **values** are already initialized

# Retrieving Data
``` python3
map.keys()     # gets keys in form of a list
map.values()   # gets values in form of a list
map.items()    # gets key and values list as tuples
```

# Time Complexity
* Read  -> O(1)
* Insert  -> O(1)
* Delete -> O(1)