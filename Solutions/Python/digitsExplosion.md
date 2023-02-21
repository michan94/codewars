## Problem

Given a string made of digits [0-9], return a string where each digit is repeated a number of times equals to its value.

## Examples

explode("312")
should return :

"333122"
explode("102269")
should return :

"12222666666999999999"

**Solution 1:**

```python
def explode(s):
    result = ''
    for num in s:
        result += int(num)*num
    return result
```

**Solution 2:**

```python
def explode(s):
    return ''.join(c * int(c) for c in s)
```
