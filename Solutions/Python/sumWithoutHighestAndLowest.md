## Problem

Sum all the numbers of a given array ( cq. list ), except the highest and the lowest element ( by value, not by index! ).

The highest or lowest element respectively is a single element at each edge, even if there are more than one with the same value.

Mind the input validation.

- If an empty value ( null, None, Nothing etc. ) is given instead of an array, or the given array is an empty list or a list with only 1 element, return 0.

## Example

{ 6, 2, 1, 8, 10 } => 16
{ 1, 1, 11, 2, 3 } => 6

**First Solution:**

```python
def sum_array(arr):
    if not arr or len(arr) < 3:
        return 0
    highest, lowest = max(arr), min(arr)
    arr.remove(highest)
    arr.remove(lowest)
    return sum(arr)
```

**Second Solution:**

```python
def sum_array(arr):
    if not arr or len(arr) < 3:
        return 0
    arr.sort()
    return sum(arr[1:len(arr)-1])
```
