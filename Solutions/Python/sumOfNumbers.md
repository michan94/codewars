## Problem

Given two integers a and b, which can be positive or negative, find the sum of all the integers between and including them and return it. If the two numbers are equal return a or b.

Note: a and b are not ordered!

## Example

(1, 0) --> 1 (1 + 0 = 1)
(1, 2) --> 3 (1 + 2 = 3)
(0, 1) --> 1 (0 + 1 = 1)
(1, 1) --> 1 (1 since both are same)
(-1, 0) --> -1 (-1 + 0 = -1)
(-1, 2) --> 2 (-1 + 0 + 1 + 2 = 2)

**First Solution:**

```python
def get_sum(a,b):
    if a == b:
        return a
    result = 0
    if a < b:
        for i in range(a,b+1):
            result += i
    else:
        for i in range(b,a+1):
            result += i
    return result
```

**Second Solution:**

```python
def get_sum(a,b):
    if a == b:
        return a
    result = 0
    for i in range(min(a,b),max(a,b)+1):
        result += i
    return result
```
