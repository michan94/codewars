## Problem

Given a sequence of numbers, find the largest pair sum in the sequence.

## Example

[10, 14, 2, 23, 19] --> 42 (= 23 + 19)
[99, 2, 2, 23, 19] --> 122 (= 99 + 23)
Input sequence contains minimum two elements and every element is an integer.

**First Solution:**

```python
def largest_pair_sum(numbers):
    if len(numbers) < 2:
        return -1

    largest = max(numbers)
    numbers.remove(largest)
    return largest + max(numbers)
```
