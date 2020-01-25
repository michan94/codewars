## Problem

Give you two strings: s1 and s2. If they are opposite, return true; otherwise, return false. Note: The result should be a boolean value, instead of a string.

The opposite means: All letters of the two strings are the same, but the case is opposite. you can assume that the string only contains letters or it's a empty string. Also take note of the edge case - if both strings are empty then you should return false/False.

### Examples:

isOpposite("ab","AB") should return true;

isOpposite("aB","Ab") should return true;

isOpposite("aBcd","AbCD") should return true;

isOpposite("AB","Ab") should return false;

isOpposite("","") should return false;

**First Solution:**
```python
def is_opposite(s1,s2):
  if len(s1) == 0 or len(s2) == 0:
    return False;
  oppS2 = "";
  s2 = list(s2);
  for letter in s2:
    if (letter == letter.lower()):
      oppS2 += letter.upper();
    if (letter == letter.upper()):
      oppS2 += letter.lower();
  if s1 == oppS2:
    return True;
  else:
    return False;
```