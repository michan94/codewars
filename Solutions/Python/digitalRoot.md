## Problem

In this kata, you must create a digital root function.

A digital root is the recursive sum of all the digits in a number. Given n, take the sum of the digits of n. If that value has more than one digit, continue reducing in this way until a single-digit number is produced. This is only applicable to the natural numbers.

**First Solution:**
```python
def digital_root(n):
  dRoot = 0;
  n = str(n);
  for num in n:
    dRoot += int(num);
  if len(str(dRoot)) > 1:
    return digital_root(int(dRoot));
  else:
    return dRoot;
```