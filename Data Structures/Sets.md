* No duplicates 
* Unordered
* dynamic shrink or grow
* One typically tests a value for membership in a set.
* Set is implemented as a hash table in Python
	* lookup/insert/delete in **O(1)** average

Good to remember 
``` python
s =  'raul'
sett = set(s[0:3])
# {'u','r','a'}

sett.add(s[0:3])
# {'rau'}
```
