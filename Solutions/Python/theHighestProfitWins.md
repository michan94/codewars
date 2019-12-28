## Problem

Write a function that returns both the minimum and maximum number of the given list/array.

### Example

* min_max([1,2,3,4,5])   == [1,5]

* min_max([2334454,5])   == [5, 2334454]

* min_max([1])           == [1, 1]




**First Solution:**
```python
def min_max(lst):
  minimum = min(lst);
  maximum = max(lst);
  return [minimum, maximum];
```


**Second Solution:**
```python
def min_max(lst):
  minimum = lst[0];
  maximum = lst[0];
  if len(lst) > 0:			#Maybe should be len(lst) > 1
    for price in lst:
      if price < minimum:
        minimum = price;
      if price > maximum:
        maximum = price;
  return [minimum, maximum]
```
