## Problem

Given an array/list of integers, find the Nth smallest element in the array.

Notes

Array/list size is at least 3.
Array/list's numbers could be a mixture of positives , negatives and zeros.
Repetition in array/list's numbers could occur, so don't remove duplications.

## Examples

arr=[3,1,2] n=2 ==> return 2
arr=[15,20,7,10,4,3] n=3 ==> return 7
arr=[2,169,13,-5,0,-1] n=4 ==> return 2
arr=[2,1,3,3,1,2], n=3 ==> return 2

**Solution 1:**

```python
def nth_smallest(arr, pos):
    arr.sort()
    for i in range(pos-1):
        arr.pop(0)
    return arr.pop(0)
```
