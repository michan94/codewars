## Problem

In this Kata your task will be to return the count of pairs that have consecutive numbers as follows:

pairs([1,2,5,8,-4,-3,7,6,5]) = 3

The pairs are selected as follows [(1,2),(5,8),(-4,-3),(7,6),5]
--the first pair is (1,2) and the numbers in the pair are consecutive; Count = 1
--the second pair is (5,8) and are not consecutive
--the third pair is (-4,-3), consecutive. Count = 2
--the fourth pair is (7,6), also consecutive. Count = 3.
--the last digit has no pair, so we ignore.

**Solution 1:**

```python
def pairs(ar):
    if len(ar) < 2:
        return 0

    count = 0
    left, right = 0, 1
    while right < len(ar):
        if abs(ar[right] - ar[left]) == 1:
            count += 1
        left += 2
        right += 2
    return count
```
