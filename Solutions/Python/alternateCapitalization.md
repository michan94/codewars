## Problem

Given a string, capitalize the letters that occupy even indexes and odd indexes separately, and return as shown below. Index 0 will be considered even.

For example, capitalize("abcdef") = ['AbCdEf', 'aBcDeF']. See test cases for more examples.

The input will be a lowercase string with no spaces.

Good luck!

**First Solution:**

```python
def capitalize(s):
    firstCap = secondCap = ''
    for i in range(len(s)):
        if i % 2 == 0:
            firstCap += s[i].upper()
            secondCap += s[i].lower()
        else:
            firstCap += s[i].lower()
            secondCap += s[i].upper()
    return [firstCap, secondCap]
```

**Second Solution:**

```python
def capitalize(s):
    firstCap = ''
    for i in range(len(s)):
        if i % 2 == 0:
            firstCap += s[i].upper()
        else:
            firstCap += s[i].lower()
    return [firstCap, firstCap.swapcase()]
```
