## Problem

Complete the function which takes two arguments and returns all numbers which are divisible by the given divisor. First argument is an array of numbers and the second is the divisor.

### Example

* divisible_by([1, 2, 3, 4, 5, 6], 2) == [2, 4, 6]



**First Solution:**
```python
def divisible_by(numbers, divisor):
  result = [];
  for num in numbers:
    if num % divisor == 0:
      result.append(num);
  return result;
```
