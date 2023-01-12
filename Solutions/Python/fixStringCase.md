## Problem

In this Kata, you will be given a string that may have mixed uppercase and lowercase letters and your task is to convert that string to either lowercase only or uppercase only based on:

make as few changes as possible.
if the string contains equal number of uppercase and lowercase letters, convert the string to lowercase.

## Examples

solve("coDe") = "code". Lowercase characters > uppercase. Change only the "D" to lowercase.
solve("CODe") = "CODE". Uppercase characters > lowecase. Change only the "e" to uppercase.
solve("coDE") = "code". Upper == lowercase. Change all to lowercase.

**First Solution:**

```python
def solve(s):
    numLower = numUpper = 0
    for letter in s:
        if letter.isupper():
            numUpper += 1
        else:
            numLower += 1
    if numLower >= numUpper:
        return s.lower()
    return s.upper()
```
