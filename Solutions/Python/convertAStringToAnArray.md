## Problem

Write a function to split a string and convert it into an array of words

## Example

* "Robin Singh" ==> ["Robin", "Singh"]

* "I love arrays they are my favorite" ==> ["I", "love", "arrays", "they", "are", "my", "favorite"]

**First Solution:**
```python
def string_to_array(s):
  if s == "":
    return [""];
  else:
    return s.split();
```    
