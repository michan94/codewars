## Problem

Write a function that will return the count of distinct case-insensitive alphabetic characters and numeric digits that occur more than once in the input string. The input string can be assumed to contain only alphabets (both uppercase and lowercase) and numeric digits.

## Examples

"abcde" -> 0 # no characters repeats more than once
"aabbcde" -> 2 # 'a' and 'b'
"aabBcde" -> 2 # 'a' occurs twice and 'b' twice (`b` and `B`)
"indivisibility" -> 1 # 'i' occurs six times
"Indivisibilities" -> 2 # 'i' occurs seven times and 's' occurs twice
"aA11" -> 2 # 'a' and '1'
"ABBA" -> 2 # 'A' and 'B' each occur twice

**Solution 1:**

```python
def duplicate_count(text):
    seen = {}
    count = 0
    for ch in text.lower():
        if ch in seen:
            seen[ch] += 1
        else:
            seen[ch] = 1
    for key,val in seen.items():
        if val > 1:
            count += 1
    return count
```
