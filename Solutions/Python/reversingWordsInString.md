## Problem

You need to write a function that reverses the words in a given string. A word can also fit an empty string. If this is not clear enough, here are some examples:

As the input may have trailing spaces, you will also need to ignore unneccesary whitespace.

## Examples

"Hello World" --> "World Hello"
"Hi There." --> "There. Hi"

**Solution 1:**

```python
def reverse(st):
    words = st.strip().split()
    return ' '.join(word for word in words[::-1])
```
