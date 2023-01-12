## Problem

Remove an exclamation mark from the end of a string. For a beginner kata, you can assume that the input data is always a string, no need to verify it.

## Examples

remove("Hi!") == "Hi"
remove("Hi!!!") == "Hi!!"
remove("!Hi") == "!Hi"
remove("!Hi!") == "!Hi"
remove("Hi! Hi!") == "Hi! Hi"
remove("Hi") == "Hi"

**First Solution:**

```python
def remove(s):
    if not s:
        return ''

    if s[len(s)-1] == '!':
        return s[:len(s)-1]
    return s
```
