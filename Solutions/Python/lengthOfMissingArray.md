## Problem

**Solution 1:**

```python
def get_length_of_missing_array(array_of_arrays):
    if not array_of_arrays:
        return 0

    lengths = []
    for arr in array_of_arrays:
        if not arr:
            return 0
        lengths.append(len(arr))
    for i in range(min(lengths),max(lengths)):
        if i not in lengths:
            return i
    return -1
```
