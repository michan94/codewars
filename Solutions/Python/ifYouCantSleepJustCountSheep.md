## Problem

If you can't sleep, just count sheep!!

Task:

Given a non-negative integer, 3 for example, return a string with a murmur: "1 sheep...2 sheep...3 sheep...". Input will always be valid, i.e. no negative integers.


**First Solution:**
```python
def count_sheep(n):
  result = "";
  count = 1;
  while count <= n:
    result += str(count) + " sheep...";
    count += 1;
  return result;
```