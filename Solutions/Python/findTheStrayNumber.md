## Problem

You are given an odd-length array of integers, in which all of them are the same, except for one single number.

Complete the method which accepts such an array, and returns that single different number.

The input array will always be valid! (odd-length >= 3)

### Examples

[1, 1, 2] ==> 2

[17, 17, 3, 17, 17, 17, 17] ==> 3

**First Solution:**
```python
def stray(arr):
  result = {};
  for num in arr:
    if num not in result:
      result[num] = 1;
    else:
      result[num] += 1;
  for key, value in result.items():
    if value == 1:
      return key;
```