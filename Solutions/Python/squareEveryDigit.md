## Problem

Welcome. In this kata, you are asked to square every digit of a number.

Note: The function accepts an integer and returns an integer

###Ex: 

* square_digits(9119) == 811181

**First Solution:**
```python
def square_digits(num):
    numString = list(str(num)); 	#Splits num into digits
    result = "";
    for digit in numString:
      result += str(int(digit)**2)	#Square every digit, convert back to string, and add to new string
    return int(result);
```
