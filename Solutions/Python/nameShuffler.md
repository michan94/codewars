## Problem

Write a function that returns a string in which firstname is swapped with last name.

## Example

"john McClane" --> "McClane john"

**First Solution:**

```python
def name_shuffler(str_):
    names = str_.split()
    return ' '.join(names[::-1])
```
