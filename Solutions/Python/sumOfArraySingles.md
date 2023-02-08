## Problem

In this Kata, you will be given an array of numbers in which two numbers occur once and the rest occur only twice. Your task will be to return the sum of the numbers that occur only once.

For example, repeats([4,5,7,5,4,8]) = 15 because only the numbers 7 and 8 occur once, and their sum is 15. Every other number occurs twice.

**Solution 1:**

```python
def repeats(arr):
    frequency = {}
    total = 0
    for num in arr:
        if num in frequency:
            frequency[num] += 1
        else:
            frequency[num] = 1
    for key,val in frequency.items():
        if val == 1:
            total += key
    return total
```
