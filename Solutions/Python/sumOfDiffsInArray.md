## Problem

Your task is to sum the differences between consecutive pairs in the array in descending order.

## Example

[2, 1, 10] --> 9
In descending order: [10, 2, 1]

Sum: (10 - 2) + (2 - 1) = 8 + 1 = 9

If the array is empty or the array has only one element the result should be 0 (Nothing in Haskell, None in Rust).

**Solution 1:**

```python
def sum_of_differences(arr):
    if len(arr) < 2:
        return 0
    arr.sort(reverse=True)
    sums=[]
    left, right = 0, 1
    while right < len(arr):
        sums.append(arr[left] - arr[right])
        left += 1
        right += 1
    return sum(sums)
```

**Solution 2:**

```python
def sum_of_differences(arr):
    if len(arr) < 2:
        return 0
    arr.sort(reverse=True)
    total, left, right = 0, 0, 1
    while right < len(arr):
        total += arr[left]-arr[right]
        left += 1
        right += 1
    return total
```

**Solution 3:**

```python
def sum_of_differences(arr):
    return max(arr) - min(arr) if arr else 0
```
