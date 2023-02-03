## Problem

Write a function that takes a string and outputs a strings of 1's and 0's where vowels become 1's and non-vowels become 0's.

All non-vowels including non alpha characters (spaces,commas etc.) should be included.

## Examples:

vowelOne "abceios" -- "1001110"

vowelOne "aeiou, abc" -- "1111100100"

**Solution 1:**

```python
def vowel_one(s):
    result, vowels = '','aeiou'
    for letter in s:
        if letter.lower() in vowels:
            result += '1'
        else:
            result += '0'
    return result
```

**Solution 2:**

```python
def vowel_one(s):
    return "".join("1" if letter in "aeiou" else "0" for letter in s.lower())
```
