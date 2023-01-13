## Problem

This is the first step to understanding FizzBuzz.

Your inputs: a positive integer, n, greater than or equal to one. n is provided, you have NO CONTROL over its value.

Your expected output is an array of positive integers from 1 to n (inclusive).

Your job is to write an algorithm that gets you from the input to the output.

**First Solution:**

```python
def pre_fizz(n):
    result = []
    for i in range(1,n+1):
        result.append(i)
    return result
```
