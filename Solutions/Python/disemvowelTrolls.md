## Problem

You are going to be given a word. Your job is to return the middle character of the word. If the word's length is odd, return the middle character. If the word's length is even, return the middle 2 characters.

### Example

* Kata.getMiddle("test") should return "es"

* Kata.getMiddle("testing") should return "t"

* Kata.getMiddle("middle") should return "dd"

* Kata.getMiddle("A") should return "A"


**First Solution:**
```python
def get_middle(s):
  lower = 0;
  upper = len(s) - 1;
  difference = upper - lower;
  result = "";
  if len(s) == 1:
    return s;
  if len(s) % 2 == 0:        #If word length even
    while difference != 1:
      lower += 1;
      upper -= 1;
      difference = upper - lower;
    result += s[lower];
    result += s[upper];
  else:
    result += s[int(len(s) / 2)];
  return result;
```

**Second Solution:**
```python
def get_middle(s):
  if len(s) == 1:
    return s;
  if len(s) % 2 != 0:
    return s[int(len(s) / 2)];
  if len(s) %2 == 0:
    return s[int((len(s) / 2) - 1)] + s[int(len(s) / 2)];
```



