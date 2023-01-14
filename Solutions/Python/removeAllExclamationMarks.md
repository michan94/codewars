## Problem

Remove all exclamation marks from the end of sentence.

## Examples

remove("Hi!") === "Hi"
remove("Hi!!!") === "Hi"
remove("!Hi") === "!Hi"
remove("!Hi!") === "!Hi"
remove("Hi! Hi!") === "Hi! Hi"
remove("Hi") === "Hi"

**Solution 1:**

```python
def remove(s):
    return s.rstrip('!')
```
