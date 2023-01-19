## Problem

Write a program to determine if a string contains only unique characters. Return true if it does and false otherwise.

The string may contain any of the 128 ASCII characters. Characters are case-sensitive, e.g. 'a' and 'A' are considered different characters.

**Solution 1:**

```python
def has_unique_chars(string):
    seen = set()
    for letter in string:
        if letter in seen:
            return False
        seen.add(letter)
    return True
```
