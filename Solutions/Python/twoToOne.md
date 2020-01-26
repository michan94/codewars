## Problem

Take 2 strings s1 and s2 including only letters from ato z. Return a new sorted string, the longest possible, containing distinct letters,

each taken only once - coming from s1 or s2.

### Examples:

a = "xyaabbbccccdefww"

b = "xxxxyyyyabklmopq"

longest(a, b) -> "abcdefklmopqwxy"


a = "abcdefghijklmnopqrstuvwxyz"

longest(a, a) -> "abcdefghijklmnopqrstuvwxyz"



**First Solution:**
```python
def longest(s1, s2):
  used = [];
  result = "";
  total = s1 + s2;    #sorting letters
  total = list(total);
  total.sort();
  for letter in total[:len(total)]:
    if letter not in used:
      result += letter;
      used.append(letter);
    else:
      continue;
  return result;
```