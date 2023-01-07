## Problem

Write a function consonantCount, consonant_count or ConsonantCount that takes a string of English-language text and returns the number of consonants in the string.

Consonants are all letters used to write English excluding the vowels a, e, i, o, u.

**First Solution:**

```python
def consonant_count(s):
    vowels = 'aeiou'
    result = 0
    s = s.replace(" ", "").lower()
    for letter in s:
        if letter not in vowels and not letter.isnumeric() and letter.isalnum():
            result += 1
    return result
```
