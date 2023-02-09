## Problem

Write a method, that gets an array of integer-numbers and return an array of the averages of each integer-number and his follower, if there is one.

## Example:

Input: [ 1, 3, 5, 1, -10]
Output: [ 2, 4, 3, -4.5]

If the array has 0 or 1 values or is null, your method should return an empty array.

**Solution 1:**

```python
def averages(arr):
    if not arr or len(arr) < 2:
        return []

    result = []
    for i in range(len(arr)-1):
        result.append((arr[i]+arr[i+1])/2)
    return result
```
