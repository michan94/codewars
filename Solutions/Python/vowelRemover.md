## Problem

Create a function called shortcut to remove the lowercase vowels (a, e, i, o, u ) in a given string.

### Examples

"hello" --> "hll"
"codewars" --> "cdwrs"
"goodbye" --> "gdby"
"HELLO" --> "HELLO"

**First Solution:**

```python
def shortcut( s ):
    vowels = ['a','e','i','o','u']
    result = ''
    for letter in s:
        if letter not in vowels:
            result += letter
    return result
```
