## Problem

Challenge:

Given a two-dimensional array of integers, return the flattened version of the array with all the integers in the sorted (ascending) order.

## Example

Given [[3, 2, 1], [4, 6, 5], [], [9, 7, 8]], your function should return [1, 2, 3, 4, 5, 6, 7, 8, 9].

**First Solution:**

```python
def flatten_and_sort(array):
    result = []
    for i in range(len(array)):
        for j in range(len(array[i])):
            result.append(array[i][j])
    return sorted(result)
```

**Second Solution:**

```python
def flatten_and_sort(array):
    return sorted([j for i in array for j in i])
```
