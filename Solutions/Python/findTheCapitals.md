## Problem

Write a function that takes a single string (word) as argument. The function must return an ordered list containing the indexes of all capital letters in the string.

## Example

Test.assertSimilar( capitals('CodEWaRs'), [0,3,4,6] );

**First Solution:**

```python
def capitals(word):
    indices = []
    for i in range(len(word)):
        if word[i] == word[i].upper():
            indices.append(i)
    return indices
```

**Second Solution:**

```python
def capitals(word):
    indices = []
    for i in range(len(word)):
        if word[i].isupper()
            indices.append(i)
    return indices
```
