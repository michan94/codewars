## Problem

Return an array containing the numbers from 1 to N, where N is the parametered value.

Replace certain values however if any of the following conditions are met:

If the value is a multiple of 3: use the value "Fizz" instead
If the value is a multiple of 5: use the value "Buzz" instead
If the value is a multiple of 3 & 5: use the value "FizzBuzz" instead
N will never be less than 1.

## Example

fizzbuzz(3) --> [1, 2, "Fizz"]

**Solution 1:**

```python
def fizzbuzz(n):
    result = []
    for i in range(1,n+1):
        if i % 3 == 0:
            if i % 5 == 0:
                result.append('FizzBuzz')
            else:
                result.append('Fizz')
        elif i % 5 == 0:
            if i % 3 == 0:
                result.append('FizzBuzz')
            else:
                result.append('Buzz')
        else:
            result.append(i)
    return result
```

**Solution 2:**

```python
def fizzbuzz(n):
    result = []
    for i in range (1, n+1):
        if i % 3 == 0 and i % 5 == 0:
            result.append("FizzBuzz")
        elif i % 3 == 0:
            result.append("Fizz")
        elif i % 5 == 0:
            result.append("Buzz")
        else:
            result.append(i)
    return result
```
