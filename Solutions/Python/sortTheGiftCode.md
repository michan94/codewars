## Problem

Write a function called sortGiftCode/sort_gift_code/SortGiftCode that accepts a string containing up to 26 unique alphabetical characters, and returns a string containing the same characters in alphabetical order.

## Examples

"abcdef" -- => "abcdef"
"pqksuvy" -- => "kpqsuvy"
"zyxwvutsrqponmlkjihgfedcba" -- => "abcdefghijklmnopqrstuvwxyz"

**Solution 1:**

```python
def sort_gift_code(code):
    return ''.join(sorted(code))
```
