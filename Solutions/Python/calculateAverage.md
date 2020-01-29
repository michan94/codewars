## Problem

Write function avg which calculates average of numbers in given list.

Python:

Due to rounding issues please do not use statistics.mean or such.
If the array is empty, return 0.



**First Solution:**
```python
def find_average(array):
  sum = 0;
  total = len(array);
  if total == 0:
  	return 0;
  for num in array:
    sum += num;
  return sum / total;
```