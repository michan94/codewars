## Problem

A number is a Special Number if it’s digits only consist 0, 1, 2, 3, 4 or 5

Given a number determine if it special number or not .

**First Solution:**
```python
def special_number(number):
  special = "012345";
  special.split();
  number = str(number);
  for digit in number:
    if digit not in special:
      return "NOT!!";
    else:
      continue;
  return "Special!!";
```