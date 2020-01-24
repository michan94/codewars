## Problem

You will be given an array a and a value x. All you need to do is check whether the provided array contains the value.

Array can contain numbers or strings. X can be either.

Return true if the array contains the value, false if not.


**First Solution:**
```python
def check(seq, elem):
  for element in seq:
    if element == elem:
      return True;
    continue;
  return False;
```