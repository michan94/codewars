## Problem

Implement a function that accepts 3 integer values a, b, c. The function should return true if a triangle can be built with the sides of given length and false in any other case.

(In this case, all triangles must have surface greater than 0 to be accepted).

**Solution 1:**

```python
def is_triangle(a, b, c):
    if not a or not b or not c:
        return False
    if a + b > c:
        if a + c > b:
            if b + c > a:
                return True
    return False
```
