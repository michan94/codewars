## Problem

Return the number (count) of vowels in the given string.

We will consider a, e, i, o, and u as vowels for this Kata.

The input string will only consist of lower case letters and/or spaces.

**First Solution:**
```python
def getCount(inputStr):
    num_vowels = 0
    vowels = "aeiou";
    valid_vowels = list(vowels);
    str = list(inputStr);
    for letter in str:
        if letter in valid_vowels:
            num_vowels += 1;
    return num_vowels     
```
