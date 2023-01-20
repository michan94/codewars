## Problem

Complete the function that accepts a string parameter, and reverses each word in the string. All spaces in the string should be retained.

## Examples

"This is an example!" ==> "sihT si na !elpmaxe"
"double spaces" ==> "elbuod secaps"

**Solution 1:**

```python
def reverse_words(text):
    words = text.split()
    return ' '.join(word[::-1] for word in words)
```
