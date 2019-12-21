## Problem

It's pretty straightforward. Your goal is to create a function that removes the first and last characters of a string. You're given one parameter, the original string. You don't have to worry with strings with less than two characters.


**First Solution:**
```python
def remove_char(s):
    t = s;
    t = s[1:len(s)-1];
    return t;     
```
