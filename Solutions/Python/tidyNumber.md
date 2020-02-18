## Problem

A Tidy number is a number whose digits are in non-decreasing order.

Given a number, Find if it is Tidy or not .


**First Solution:**
```python
def tidyNumber(n):
  print(n)
  n = str(n);
  for i in range(0,len(n)-1):
    if n[int(i)] <= n[int(i + 1)]:
      print(n[int(i)])
      print(n[int(i+1)])
      continue;
    else:
      return False;
  return True;
```
