## Problem

Given a non-empty array of integers, return the result of multiplying the values together in order. Example:

[1, 2, 3, 4] => 1 * 2 * 3 * 4 = 24

**First Solution:**
```python
def grow(arr):
  total = 1;
  for num in arr:
    total *= num;
  return total;
```