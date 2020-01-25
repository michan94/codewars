## Problem

Take an array and remove every second element out of that array. Always keep the first element and start removing with the next element.

**First Solution:**
```python
def remove_every_other(my_list):
  result = [];
  for item in my_list[::2]:
    result.append(item);
  return result;
```