## Problem

Given a Divisor and a Bound , Find the largest integer N , Such That ,

Conditions :

N is divisible by divisor

N is less than or equal to bound

N is greater than 0.

## Example

* maxMultiple (2,7) ==> return (6)

* maxMultiple (10,50)  ==> return (50)

**First Solution**
```python
def max_multiple(divisor, bound):
  largest = divisor; 
  for i in range(divisor, bound + 1):
    if (i % divisor == 0):
        if (i <= bound):
            if (i > 0):
                if i > largest:
                    largest = i;
  return largest;
```