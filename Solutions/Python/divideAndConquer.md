## Problem

Given a mixed array of number and string representations of integers, add up the string integers and subtract this from the total of the non-string integers.

Return as a number.

### Examples

* div_con([9, 3, '7', '3']) --> 2

**First Solution:**
```python
def div_con(x):
  nonString = 0;
  stringNum = 0;
  for element in x:
    if type(element) == int:
      nonString += element;
    if type(element) == str:
      stringNum += int(element);
  return nonString - stringNum; 
```
