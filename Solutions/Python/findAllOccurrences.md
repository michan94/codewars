## Problem

Given an array (a list in Python) of integers and an integer n, find all occurrences of n in the given array and return another array containing all the index positions of n in the given array.

If n is not in the given array, return an empty array [].

Assume that n and all values in the given array will always be integers.

### Example

*  find_all([6, 9, 3, 4, 3, 82, 11], 3) ==> [2, 4]


**First Solution:**
```python
def find_all(array, n):
  indices = [];
  if n not in array:
    return [];
  else:
    for i in range(len(array)):
      if array[i] == n:
        indices.append(i);
    return indices;
```
