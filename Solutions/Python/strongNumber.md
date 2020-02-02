## Problem

Strong number is the number that the sum of the factorial of its digits is equal to number itself.

Given a number, Find if it is Strong or not.

For example: 145, since

1! + 4! + 5! = 1 + 24 + 120 = 145

So, 145 is a Strong number.




**First Solution:**
```python
def strong_num(number):
  factorial = 0;
  number = str(number);
  for digit in number:
    digit = int(digit)
    temp = 1;
    while digit > 0:
      temp *= digit;
      digit -= 1;
    factorial += temp;
  if factorial == int(number):
    return "STRONG!!!!"
  else:
    return "Not Strong !!"
```