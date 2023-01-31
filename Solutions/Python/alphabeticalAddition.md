## Problem

Write a function that finds the sum of all its arguments.

## Examples

sum_args(1, 2, 3) # => 6
sum_args(8, 2) # => 10
sum_args(1, 2, 3, 4, 5) # => 15

**Solution 1:**

```python
def add_letters(*letters):
    if not letters:
        return 'z'

    alphabet = {'a': 1, 'c': 3, 'b': 2, 'e': 5, 'd': 4, 'g': 7, 'f': 6, 'i': 9, 'h': 8, 'k': 11, 'j': 10, 'm': 13, 'l': 12, 'o': 15, 'n': 14, 'q': 17, 'p': 16, 's': 19, 'r': 18, 'u': 21, 't': 20, 'w': 23, 'v': 22, 'y': 25, 'x': 24, 'z': 26}
    total = 0
    for ch in letters:
        total += alphabet[ch]
    while total > 26:
        total -= 26
    return get_key(total)

def get_key(val):
    alphabet = {'a': 1, 'c': 3, 'b': 2, 'e': 5, 'd': 4, 'g': 7, 'f': 6, 'i': 9, 'h': 8, 'k': 11, 'j': 10, 'm': 13, 'l': 12, 'o': 15, 'n': 14, 'q': 17, 'p': 16, 's': 19, 'r': 18, 'u': 21, 't': 20, 'w': 23, 'v': 22, 'y': 25, 'x': 24, 'z': 26}
    for key, value in alphabet.items():
        if val == value:
            return key
```

**Solution 2**

```python
num = 'abcdefghijklmnopqrstuvwxyz'
def add_letters(*letters):
    x = sum(num.index(i)+1 for i in letters)
    while x > 26:
        x -= 26
    return num[x-1]
```
