## Problem

Create a function add(n)/Add(n) which returns a function that always adds n to any number

Note for Java: the return type and methods have not been provided to make it a bit more challenging.

## Examples

add_one = add(1)
add_one(3) # 4

add_three = add(3)
add_three(3) # 6

**Solution 1:**

```python
def add(n):
    def add_whatever(i):
        return n + i
    return add_whatever
```
