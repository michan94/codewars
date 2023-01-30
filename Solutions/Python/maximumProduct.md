## Problem

Given an array of integers , Find the maximum product obtained from multiplying 2 adjacent numbers in the array.

Notes

Array/list size is at least 2.
Array/list numbers could be a mixture of positives, negatives also zeroes .

## Examples

adjacentElementsProduct([1, 2, 3]); ==> return 6
adjacentElementsProduct([9, 5, 10, 2, 24, -1, -48]); ==> return 50
adjacentElementsProduct([-23, 4, -5, 99, -27, 329, -2, 7, -921]) ==> return -14

**Solution 1:**

```python
def adjacent_element_product(array):
    if len(array) < 2:
        return -1

    left, right = 0, 1
    result = float('-inf')
    while right < len(array):
        temp = array[left] * array[right]
        if temp > result:
            result = temp
        left += 1
        right += 1
    return result
```
