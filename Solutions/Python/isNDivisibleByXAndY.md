## Problem

Create a function that checks if a number n is divisible by two numbers x AND y. All inputs are positive, non-zero digits.

**First Solution:**
```python
def is_divisible(n,x,y):
    divByX = False;
    divByY = False;
    
    if (n % x == 0):
      divByX = True;
    if (n % y == 0):
      divByY = True;
    return (divByX and divByY);
```
