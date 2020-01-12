## Problem

Convert number to reversed array of digits
Given a random number:

C#: long;
C++: unsigned long;
You have to return the digits of this number within an array in reverse order.

### Example

* 348597 => [7,9,5,8,4,3]



**First Solution:**
```python
def digitize(n):
  result = [];
  n = list(str(n));
  for digit in reversed(n):
    result.append(int(digit));
  return result;
```
