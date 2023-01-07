## Problem

This time no story, no theory. The examples below show you how to write function accum:

## Examples:

accum("abcd") -> "A-Bb-Ccc-Dddd"
accum("RqaEzty") -> "R-Qq-Aaa-Eeee-Zzzzz-Tttttt-Yyyyyyy"
accum("cwAt") -> "C-Ww-Aaa-Tttt"

The parameter of accum is a string which includes only letters from a..z and A..Z.

**First Solution:**

```python
def accum(s):
    result = ''
    for i in range(len(s)):
        count = 0
        result += s[i].upper()
        while count < i:
            result += s[i].lower()
            count += 1
        result += '-'
    return result[:len(result)-1]
```
