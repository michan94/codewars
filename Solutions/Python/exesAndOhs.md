## Problem

Check to see if a string has the same amount of 'x's and 'o's. The method must return a boolean and be case insensitive. The string can contain any char.

### Example

* XO("ooxx") => true

* XO("xooxx") => false

* XO("ooxXm") => true

* XO("zpzpzpp") => true // when no 'x' and 'o' is present should return true

* XO("zzoo") => false

**First Solution:**
```python
def xo(s):
  lowerCaseString = s.lower();
  numX = 0;
  numO = 0;
  sameNum = True;
  for letter in lowerCaseString:
    if letter == "x":
      numX += 1;
    if letter == "o":
      numO += 1;
  if numX != numO:
    sameNum = False;
  return sameNum; 
```
