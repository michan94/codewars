## Problem

You are given an array (which will have a length of at least 3, but could be very large) containing integers. The array is either entirely comprised of odd integers or entirely comprised of even integers except for a single integer N. Write a method that takes the array as an argument and returns this "outlier" N.

## Examples

[2, 4, 0, 100, 4, 11, 2602, 36]
Should return: 11 (the only odd number)

[160, 3, 1719, 19, 11, 13, -21]
Should return: 160 (the only even number)

**Solution 1:**

```python
def find_outlier(integers):
    if len(integers) < 3:
        return -1
    odd, even = 0, 0
    for i in range(3):
        if integers[i] % 2 == 0:
            even += 1
        else:
            odd += 1
    if odd > even:
        for num in integers:
            if num % 2 == 0:
                return num
    for num in integers:
        if num % 2 != 0:
            return num
    return -1
```
