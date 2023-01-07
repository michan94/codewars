## Problem

You are given a string of letters and an array of numbers.
The numbers indicate positions of letters that must be removed, in order, starting from the beginning of the array.
After each removal the size of the string decreases (there is no empty space).
Return the only letter left.

## Examples

let str = "zbk", arr = [0, 1]
str = "bk", arr = [1]
str = "b", arr = []
return 'b'

**First Solution:**

```python
def last_survivor(letters, coords):
    chars = list(letters)
    result = ''
    while coords:
        chars.pop(coords[0])
        coords.pop(0)
    for ch in chars:
        result += ch
    return result
```
