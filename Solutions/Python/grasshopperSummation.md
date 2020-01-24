## Problem

Write a program that finds the summation of every number from 1 to num. The number will always be a positive integer greater than 0.

**First Solution:**
```python
def summation(num):
  sum = 0;
  for number in range(1, num + 1):
    sum += number;
  return sum;
```    
