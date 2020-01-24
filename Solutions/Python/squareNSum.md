## Problem

Complete the square sum function so that it squares each number passed into it and then sums the results together.

For example, for [1, 2, 2] it should return 9 because 1^2 + 2^2 + 2^2 = 9.

**First Solution:**
```python
def square_sum(numbers):
  sum = 0;
  numbers = list(numbers);
  for num in numbers:
    sum += num**2;
  return sum;
```    
