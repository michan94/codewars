## Problem

You are given two arrays a1 and a2 of strings. Each string is composed with letters from a to z. Let x be any string in the first array and y be any string in the second array.

Find max(abs(length(x) − length(y)))

If a1 and/or a2 are empty return -1 in each language except in Haskell (F#) where you will return Nothing (None).

## Example:

a1 = ["hoqq", "bbllkw", "oox", "ejjuyyy", "plmiis", "xxxzgpsssa", "xxwwkktt", "znnnnfqknaz", "qqquuhii", "dvvvwz"]
a2 = ["cccooommaaqqoxii", "gggqaffhhh", "tttoowwwmmww"]
mxdiflg(a1, a2) --> 13

Bash note:
input : 2 strings with substrings separated by ,
output: number as a string
**Solution 1:**

```python
def mxdiflg(a1, a2):
    if not a1 or not a2:
        return -1

    maxA1 = maxA2 = float('-inf')
    minA1 = minA2 = float('inf')
    for word in a1:
        if len(word) > maxA1:
            maxA1 = len(word)
        if len(word) < minA1:
            minA1 = len(word)
    for word in a2:
        if len(word) > maxA2:
            maxA2 = len(word)
        if len(word) < minA2:
            minA2 = len(word)
    return max(abs(maxA1 - minA2),abs(maxA2 - minA1))
```
