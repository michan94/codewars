## Problem

If we list all the natural numbers below 10 that are multiples of 3 or 5, we get 3, 5, 6 and 9. The sum of these multiples is 23.

Finish the solution so that it returns the sum of all the multiples of 3 or 5 below the number passed in.

Note: If the number is a multiple of both 3 and 5, only count it once.



**First Solution:**
```python
def solution(number):
  found = [];
  total = 0;
  counter = 0;
  for num in range(0, number):
    if num not in found:
      if num % 3 == 0:
        total += num;
        found.append(num);
      elif num % 5 == 0:
        total += num;
        found.append(num);
    counter += 1;
  return total;
```