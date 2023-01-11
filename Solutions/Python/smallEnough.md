## Problem

You will be given an array and a limit value. You must check that all values in the array are below or equal to the limit value. If they are, return true. Else, return false.

You can assume all values in the array are numbers.

**First Solution:**

```python
def small_enough(array, limit):
    for num in array:
        if num > limit:
            return False
    return True
```
