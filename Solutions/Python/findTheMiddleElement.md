## Problem

As a part of this Kata, you need to create a function that when provided with a triplet, returns the index of the numerical element that lies between the other two elements.

The input to the function will be an array of three distinct numbers

### Example

* gimme([2, 3, 1]) => 0

* gimme([5, 10, 14]) => 1


**First Solution:**
```python
def gimme(input_array):
  copy_array = sorted(input_array);
  mid = copy_array[1];
  return input_array.index(mid);
```
