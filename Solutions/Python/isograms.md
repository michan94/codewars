## Problem

An isogram is a word that has no repeating letters, consecutive or non-consecutive. Implement a function that determines whether a string that contains only letters is an isogram. Assume the empty string is an isogram. Ignore letter case.

## Example

"Dermatoglyphics" --> true "aba" --> false "moOse" --> false (ignore letter case)

isIsogram "Dermatoglyphics" = true
isIsogram "moose" = false
isIsogram "aba" = false

**First Solution:**

```python
def is_isogram(string):
    seen = set()
    for letter in string.lower():
        if letter in seen:
            return False
        seen.add(letter)
    return True
```
