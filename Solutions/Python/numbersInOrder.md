## Problem

In this Kata, your function receives an array of integers as input. Your task is to determine whether the numbers are in ascending order. An array is said to be in ascending order if there are no two adjacent integers where the left integer exceeds the right integer in value.

For the purposes of this Kata, you may assume that all inputs are valid, i.e. arrays containing only integers.

Note that an array of 0 or 1 integer(s) is automatically considered to be sorted in ascending order since all (zero) adjacent pairs of integers satisfy the condition that the left integer does not exceed the right integer in value.

## Examples

in_asc_order([1,2,4,7,19]) # returns True
in_asc_order([1,2,3,4,5]) # returns True
in_asc_order([1,6,10,18,2,4,20]) # returns False
in_asc_order([9,8,7,6,5,4,3,2,1]) # returns False because the numbers are in DESCENDING order

**First Solution:**

```python
def in_asc_order(arr):
    if len(arr) < 2:
        return True
    left, right = 0, 1
    while right < len(arr):
        if arr[left] > arr[right]:
            return False
        left += 1
        right += 1
    return True
```
