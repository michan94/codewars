## Problem

Given a string str, reverse it omitting all non-alphabetic characters.

### Example

* For str = "krishan", the output should be "nahsirk".

* For str = "ultr53o?n", the output should be "nortlu"


**First Solution:**
```python
def reverse_letter(string):
  alphabet = list("abcdefghijklmnopqrstuvwxyz");
  reversed = "";
  for letter in string[::-1]:
    if letter in alphabet:
      reversed += letter;
  return reversed;    
```
