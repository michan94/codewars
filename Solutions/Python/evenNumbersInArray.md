## Problem

Given an array of numbers, return a new array of length number containing the last even numbers from the original array (in the same order). The original array will be not empty and will contain at least "number" even numbers.

## Examples

([1, 2, 3, 4, 5, 6, 7, 8, 9], 3) => [4, 6, 8]
([-22, 5, 3, 11, 26, -6, -7, -8, -9, -8, 26], 2) => [-8, 26]
([6, -25, 3, 7, 5, 5, 7, -3, 23], 1) => [6]

**Solution 1:**

```python
def even_numbers(arr,n):
    if not arr:
        return []

    result = []
    while len(result) != n:
        for num in arr[::-1]:
            if num%2==0:
                result.append(num)
    return result
```
