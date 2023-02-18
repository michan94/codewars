## Problem

The function must return the truncated version of the given string up to the given limit followed by "..." if the result is shorter than the original. Return the same string if nothing was truncated.

## Example:

solution('Testing String', 3) --> 'Tes...'
solution('Testing String', 8) --> 'Testing ...'
solution('Test', 8) --> 'Test'

**Solution 1:**

```python
def solution(st, limit):
    if limit >= len(st):
        return st

    result = ''
    for i in range(limit):
        result += st[i]
    return f'{result}...'
```
