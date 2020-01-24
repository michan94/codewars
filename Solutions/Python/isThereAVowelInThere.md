## Problem

Given an array of numbers, check if any of the numbers are the character codes for lower case vowels (a, e, i, o, u).

If they are, change the array value to a string of that vowel.

Return the resulting array.

**First Solution:**
```python
def is_vow(inp):
  result = [];
  inp = list(inp);
  for num in inp:
    if num == 97:
      result.append("a");
      continue;
    if num == 101:
      result.append("e");
      continue;
    if num == 105:
      result.append("i");
      continue;
    if num == 111:
      result.append("o");
      continue;
    if num == 117:
      result.append("u");
      continue;
    else:
      result.append(num);
  return result;
```

**Second Solution:**
```python
def is_vow(inp):
  result = [];
  inp = list(inp);
  for num in inp:
    if num == 97:
      result.append("a");
      continue;
    if num == 101:
      result.append("e");
      continue;
    if num == 105:
      result.append("i");
      continue;
    if num == 111:
      result.append("o");
      continue;
    if num == 117:
      result.append("u");
      continue;
    result.append(num);
  return result;
```