## Problem

The main idea is to count all the occurring characters in a string. If you have a string like aba, then the result should be {'a': 2, 'b': 1}.

What if the string is empty? Then the result should be empty object literal, {}.

**Solution 1:**

```python
def count(string):
    if not string:
        return {}
    seen = {}

    for ch in string:
        if ch in seen:
            seen[ch] += 1
        else:
            seen[ch] = 1
    return seen
```
