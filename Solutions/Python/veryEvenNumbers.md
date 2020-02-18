## Problem

Write a function that returns true if the number is a "Very Even" number.

If a number is a single digit, then it is simply "Very Even" if it itself is even.

If it has 2 or more digits, it is "Very Even" if the sum of it's digits is "Very Even".


**First Solution:**
```python
def is_very_even_number(n):
    if len(str(n)) == 1:
      if (n % 2 == 0) or (n == 0):
        return True;
      else:
        return False;
    else:
      num = 0;
      n = str(n);
      for digit in n:
        num += int(digit);
      return is_very_even_number(num);
```
