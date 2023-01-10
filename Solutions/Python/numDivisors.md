## Problem

Count the number of divisors of a positive integer n.

Random tests go up to n = 500000.

## Example

4 --> 3 (1, 2, 4)
5 --> 2 (1, 5)
12 --> 6 (1, 2, 3, 4, 6, 12)
30 --> 8 (1, 2, 3, 5, 6, 10, 15, 30)

Note you should only return a number, the count of divisors. The numbers between parentheses are shown only for you to see which numbers are counted in each case.

**First Solution:**

```python
def divisors(n):
    result = 0
    for i in range(1, n//2+1):
        if n % i == 0:
            result += 1
    # + 1 for n itself
    return result + 1
```
