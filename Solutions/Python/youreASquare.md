## Problem

Given an integral number, determine if it's a square number:

In mathematics, a square number or perfect square is an integer that is the square of an integer; in other words, it is the product of some integer with itself.

The tests will always use some integral number, so don't worry about that in dynamic typed languages.

###Ex: 

* isSquare(-1) returns  false
* isSquare(0) returns   true
* isSquare(3) returns   false
* isSquare(4) returns   true
* isSquare(25) returns  true  
* isSquare(26) returns  false

**First Solution:**
```python
def is_square(n):    
    squareNum = False;
    if n < 0:
      squareNum = False;
    if n == 0:
      squareNum = True;
    if n > 0:
      squareNum = (float(n%n**0.5)==0);
    return squareNum;
```
