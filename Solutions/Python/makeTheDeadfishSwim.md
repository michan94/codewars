## Problem

Write a simple parser that will parse and run Deadfish.

Deadfish has 4 commands, each 1 character long:

i increments the value (initially 0)
d decrements the value
s squares the value
o outputs the value into the return array

Invalid characters should be ignored.

parse("iiisdoso") ==> [8, 64]

**Solution 1:**

```python
def parse(data):
    result = []
    counter = 0
    for ch in data:
        if ch == 'i':
            counter += 1
        elif ch == 'd':
            counter -= 1
        elif ch == 's':
            counter *= counter
        elif ch == 'o':
            result.append(counter)
    return result
```
