## Problem

Your task is to write function factorial

https://en.wikipedia.org/wiki/Factorial

### Examples

* factorial(1) --> 1

* factorial(2) --> 2

**First Solution:**
```python
def factorial(n):
    if (n <= 1):
        return 1;
    else:
        return n * factorial(n-1);
```
