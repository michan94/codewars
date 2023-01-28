## Problem

Complete the method which returns the number which is most frequent in the given input array. If there is a tie for most frequent number, return the largest number among them.

Note: no empty arrays will be given.

## Examples

[12, 10, 8, 12, 7, 6, 4, 10, 12] --> 12
[12, 10, 8, 12, 7, 6, 4, 10, 12, 10] --> 12
[12, 10, 8, 8, 3, 3, 3, 3, 2, 4, 10, 12, 10] --> 3

**Solution 1:**

```python
def highest_rank(arr):
    count = {}
    frequent, highest = float('-inf'), 0
    for num in arr:
        if num in count:
            count[num] += 1
        else:
            count[num] = 1
    for key, val in count.items():
        if val > frequent:
            frequent = val
            highest = key
        if val == frequent:
            highest = max(key,highest)
    return highest
```
