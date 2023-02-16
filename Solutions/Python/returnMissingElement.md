## Problem

Our sequence given was supposed to contain all of the integers from 0 to 9 (in no particular order), but one of them seems to be missing.

Write a function that accepts a sequence of unique integers between 0 and 9 (inclusive), and returns the missing element.

## Examples:

[0, 5, 1, 3, 2, 9, 7, 6, 4] --> 8
[9, 2, 4, 5, 7, 0, 8, 6, 1] --> 3

**Solution 1:**

```python
def get_missing_element(seq):
    for i in range(max(seq)):
        if i not in seq:
            return i
    return max(seq) + 1
```

**Solution 2:**

```python
def get_missing_element(seq):
    return 45 - sum(seq)
```
