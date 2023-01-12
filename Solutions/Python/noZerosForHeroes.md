## Problem

Numbers ending with zeros are boring.

They might be fun in your world, but not here.

Get rid of them. Only the ending ones.

## Examples

1450 -> 145
960000 -> 96
1050 -> 105
-1050 -> -105

Zero alone is fine, don't worry about it. Poor guy anyway

**First Solution:**

```python
def no_boring_zeros(n):
    if n == 0:
        return n

    stringNum = str(n)
    left, right = 0, len(stringNum)-1
    while left <= right:
        if stringNum[right] == '0':
            right -= 1
        else:
            return int(stringNum[left:right+1])
    return 0
```

**Second Solution:**

```python
def no_boring_zeros(n):
    if n == 0:
        return n

    return int(str(n).rstrip('0'))
```
