## Problem

Given a string made up of letters a, b, and/or c, switch the position of letters a and b (change a to b and vice versa). Leave any incidence of c untouched.

Example:

'acb' --> 'bca'
'aabacbaa' --> 'bbabcabb'

**Solution 1:**

```python
def switcheroo(s):
    result = ''
    for letter in s:
        if letter == 'b':
            result += 'a'
        elif letter == 'a':
            result += 'b'
        else:
            result += letter
    return result
```
