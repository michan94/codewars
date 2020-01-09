## Problem

Write a function named sumDigits which takes a number as input and returns the sum of the absolute value of each of the number's decimal digits. For example:

## Example

* sum_digits(10)  # Returns 1

* sum_digits(99)  # Returns 18

* sum_digits(-32) # Returns 5

**First Solution**
```python
def sum_digits(number):
  number = abs(number);       #Make all digits positive
  total = 0;
  digits = list(str(number));
  for digit in digits:
    num = int(digit);
    total += num;
  return total;
```