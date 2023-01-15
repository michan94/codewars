## Problem

Input: Array of elements

["h","o","l","a"]

Output: String with comma delimited elements of the array in th same order.

"h,o,l,a"

**Solution 1:**

```python
def print_array(arr):
    return ",".join(str(elem) for elem in arr)
```
