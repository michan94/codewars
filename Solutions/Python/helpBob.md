## Problem

Bob is a lazy man.

He needs you to create a method that can determine how many letters and digits are in a given string.

Example:

"hel2!lo" --> 6

"wicked .. !" --> 6

"!?..A" --> 1



**First Solution:**
```python
def count_letters_and_digits(s):
  counter = 0;
  s = list(s.lower());
  valid = "abcdefghijklmnopqrstuvwxyz1234567890";
  valid.split();
  for i in s:
    if i in valid:
      counter += 1;
  return counter;
```