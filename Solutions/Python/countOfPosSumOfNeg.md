## Problem

Given an array of integers.

Return an array, where the first element is the count of positives numbers and the second element is sum of negative numbers.

If the input array is empty or null, return an empty array.

### Example

* For input [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, -11, -12, -13, -14, -15], you should return [10, -65].

**First Solution:**
```python
def count_positives_sum_negatives(arr):
  result = [];
  numPos = 0;
  sumNeg = 0;
  if len(arr) == 0:
    return [];
  for num in arr:
    if num > 0:
      numPos += 1;
    if num < 0:
      sumNeg += num;
  result.append(numPos);
  result.append(sumNeg);
  return result;   
```    
