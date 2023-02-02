## Problem

In this Kata, you will be given a string and your task will be to return a list of ints detailing the count of uppercase letters, lowercase, numbers and special characters, as follows.

## Example

Solve("\*'&ABCDabcde12345") = [4,5,5,3].

--the order is: uppercase letters, lowercase, numbers and special characters.

**Solution 1:**

```python
def solve(s):
    upper = lower = nums = special = 0
    for ch in s:
        if ord(ch) in range(48,58):
            nums += 1
        elif ord(ch) in range(65,91):
            upper += 1
        elif ord(ch) in range(97,123):
            lower += 1
        else:
            special += 1
    return [upper, lower, nums, special]
```
