## Problem

Given an array of integers, return a new array with each value doubled.

For example:

[1, 2, 3] --> [2, 4, 6]



**First Solution:**
```python
def maps(a):
  result = [];
  for num in a:
    result.append(2 * num);
  return result;
```