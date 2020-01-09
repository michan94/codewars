## Problem

Complete the function that takes two integers (a, b, where a < b) and return an array of all integers between the input parameters, including them.

### Examples

* a = 1, b = 4 --> [1, 2, 3, 4]



**First Solution:**
```python
def between(a,b):
    finalArray = [];
    for value in range(a, b + 1):
        finalArray.append(value);
    return finalArray
```
