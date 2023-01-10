## Problem

An anagram is the result of rearranging the letters of a word to produce a new word (see wikipedia).

Note: anagrams are case insensitive

Complete the function to return true if the two arguments given are anagrams of each other; return false otherwise.

## Example

"foefet" is an anagram of "toffee"

"Buckethead" is an anagram of "DeathCubeK"

**First Solution:**

```python
def is_anagram(test, original):
    if len(test) != len(original):
        return False

    test, original = test.lower(), original.lower()
    seen = {}
    for letter in original:
        if letter in seen:
            seen[letter] += 1
        else:
            seen[letter] = 1
    for letter in test:
        if letter in seen:
            seen[letter] -= 1
    for val in seen.values():
        if val != 0:
            return False
    return True
```
