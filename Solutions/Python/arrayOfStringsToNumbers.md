## Problem

Create the function that takes as a parameter a sequence of numbers represented as strings and outputs a sequence of numbers.

ie:["1", "2", "3"] to [1, 2, 3]

Note that you can receive floats as well.

**Solution 1:**

```python
def to_float_array(arr):
    return [float(number) for number in arr]
```
