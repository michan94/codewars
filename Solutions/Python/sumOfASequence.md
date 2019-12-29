## Problem

Your task is to make function, which returns the sum of a sequence of integers.

The sequence is defined by 3 non-negative values: begin, end, step.

If begin value is greater than the end, function should returns 0

### Example

* sequenceSum(2,2,2) === 2

* sequenceSum(2,6,2) === 12 // 2 + 4 + 6

* sequenceSum(1,5,1) === 15 // 1 + 2 + 3 + 4 + 5

* sequenceSum(1,5,3) === 5 // 1 + 4



**First Solution:**
```python
def sequence_sum(begin_number, end_number, step):
  total = 0;
  addBy = begin_number;
  if begin_number > end_number:
    total = 0;
  else:
    while addBy <= end_number:
      total += addBy;
      addBy += step;
  return total;
```
