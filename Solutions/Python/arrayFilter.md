## Problem

In Python, there is a built-in filter function that operates similarly to JS's filter. For more information on how to use this function, visit https://docs.python.org/3/library/functions.html#filter

## Example

The solution would work like the following:

get_even_numbers([2,4,5,6]) => [2,4,6]

**First Solution:**

```python
def get_even_numbers(arr):
    if not arr:
        return []

    result = []
    for num in arr:
        if num % 2 == 0:
            result.append(num)
    return result
```
