## Problem

Make a function that returns the value multiplied by 50 and increased by 6. If the value entered is a string it should return "Error".

**First Solution:**

```python
def problem(a):
    if type(a) is str:
        return "Error"
    return 50*a+6
```
