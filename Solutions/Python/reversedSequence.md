## Problem

Get the number n (n>0) to return the reversed sequence from n to 1.

## Example

* n=5 >> [5,4,3,2,1]


**First Solution:**
```python
def reverse_seq(n):
  result = [];
  for num in range(n,0,-1):
    result.append(num);
  return result;
```    
