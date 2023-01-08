## Problem

Write a function to convert a name into initials. This kata strictly takes two words with one space in between them.

The output should be two capital letters with a dot separating them.

## Example

Sam Harris => S.H

patrick feeney => P.F

**First Solution:**

```python
def abbrev_name(name):
    names = name.split()
    initials = ''
    for x in names:
        initials += x[0].upper() + '.'
    return initials[:len(initials)-1]
```
