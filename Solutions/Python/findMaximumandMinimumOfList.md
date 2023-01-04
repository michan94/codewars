## Problem

Your task is to make two functions ( max and min, or maximum and minimum, etc., depending on the language ) that receive a list of integers as input, and return the largest and lowest number in that list, respectively.

### Examples:

(Input -> Output)

- [4,6,2,1,9,63,-134,566] -> max = 566, min = -134
- [-52, 56, 30, 29, -54, 0, -110] -> min = -110, max = 56
- [42, 54, 65, 87, 0] -> min = 0, max = 87
- [5] -> min = 5, max = 5

**First Solution:**

```python
def minimum(arr):
    result = float('inf')
    for num in arr:
        if num < result:
            result = num
    return result

def maximum(arr):
    result = float('-inf')
    for num in arr:
        if num > result:
            result = num
    return result
```
