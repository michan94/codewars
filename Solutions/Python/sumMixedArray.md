## Problem

Given an array of integers as strings and numbers, return the sum of the array values as if all were numbers.

Return your answer as a number.


**First Solution:**
```python
def sum_mix(arr):
  sum = 0;
  for num in arr:
    sum += int(num);
  return sum;
```
