## Problem

Please write a function that sums a list, but ignores any duplicate items in the list.

For instance, for the list [3, 4, 3, 6] , the function should return 10.

**First Solution:**

```python
def sum_no_duplicates(l):
    seen = {}
    result = 0
    for num in l:
        if num in seen:
            seen[num] += 1
        else:
            seen[num] = 1
    for num in seen:
        if seen[num] == 1:
            result += num
    return result
```

**Second Solution:**

```python
def sum_no_duplicates(l):
    seen = {}
    result = 0
    for num in l:
        if num in seen:
            seen[num] += 1
        else:
            seen[num] = 1
    for key, value in seen.items():
        if value == 1:
            result += key
    return result
```
