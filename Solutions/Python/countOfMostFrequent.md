## Problem

Complete the function to find the count of the most frequent item of an array. You can assume that input is an array of integers. For an empty array return 0

## Examples

input array: [3, -1, -1, -1, 2, 3, -1, 3, -1, 2, 4, 9, 3]
ouptut: 5

**First Solution:**

```python
def most_frequent_item_count(collection):
    if not collection:
        return 0
    freq = {}
    for num in collection:
        if num in freq:
            freq[num] += 1
        else:
            freq[num] = 1
    return max(freq.values())
```
