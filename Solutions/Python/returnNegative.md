## Problem

In this simple assignment you are given a number and have to make it negative. But maybe the number is already negative?

### Examples

* make_negative(1);  # return -1

* make_negative(-5); # return -5

* make_negative(0);  # return 0


**First Solution:**
```python
def make_negative( number ):
  if number > 0:
    return number * -1;
  else:
    return number;
```    
