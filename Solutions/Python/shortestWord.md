## Problem

Simple, given a string of words, return the length of the shortest word(s).

String will never be empty and you do not need to account for different data types.

## Example

* maxMultiple (2,7) ==> return (6)

* maxMultiple (10,50)  ==> return (50)

**First Solution**
```python
def find_short(s):
  shortest = 1000;
  s = s.split(" ");
  for word in s:
    if len(word) < shortest:
      shortest = len(word);
  return shortest;
```