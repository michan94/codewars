## Problem

Your task is to remove all duplicate words from a string, leaving only single (first) words entries.

### Example:

Input:

'alpha beta beta gamma gamma gamma delta alpha beta beta gamma gamma gamma delta'

Output:

'alpha beta gamma delta'


**First Solution:**
```python
def remove_duplicate_words(s):
  nonDupes = [];
  words = s.split()
  for word in words:
    if word not in nonDupes:
      nonDupes.append(word);
  result = " ".join(nonDupes);
  return result
```
