## Problem

Given a string, you have to return a string in which each character (case-sensitive) is repeated once.

**First Solution:**

```python
def double_char(s):
    result = ''
    for ch in s:
        result += 2*ch
    return result
```

```python
def double_char(s):
    return ''.join(2*ch for ch in s)
```
