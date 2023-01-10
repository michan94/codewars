## Problem

You will be given a list of strings. You must sort it alphabetically (case-sensitive, and based on the ASCII values of the chars) and then return the first value.

The returned value must be a string, and have "\*\*\*" between each of its letters.

You should not remove or add elements from/to the array.

**First Solution:**

```python
def two_sort(array):
    array.sort()
    result = ''
    for letter in array[0]:
        result += f'{letter}***'
    return result[:len(result)-3]
```

**Second Solution:**

```python
def two_sort(array):
    array.sort()
    return '***'.join(ch for ch in array[0])
```

**Third Solution:**

```python
def two_sort(array):
    return '***'.join(ch for ch in min(array))
```
