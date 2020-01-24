## Problem

Given a string of digits, you should replace any digit below 5 with '0' and any digit 5 and above with '1'. Return the resulting string.

**First Solution:**
```python
def fake_bin(x):
  result = "";
  stringNum = x;
  for digit in stringNum:
    if int(digit) >= 5:
      result += "1";
    if int(digit) < 5:
      result += "0";
  return result;
```

**Second Solution:**
```python
def fake_bin(x):
  result = "";
  stringNum = list(x);
  for digit in stringNum:
    if int(digit) >= 5:
      result += "1";
    if int(digit) < 5:
      result += "0";
  return result;
```