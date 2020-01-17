## Problem

Your team is writing a fancy new text editor and you've been tasked with implementing the line numbering.

Write a function which takes a list of strings and returns each line prepended by the correct number.

The numbering starts at 1. The format is n: string. Notice the colon and space in between.

## Example

* number([]) # => []

* number(["a", "b", "c"]) # => ["1: a", "2: b", "3: c"]

**First Solution:**
```python
def number(lines):
  counter = 1;
  result = [];
  if len(lines) == 0:
    return [];
  for element in lines:
    result.append(str(counter) + ": " + element);
    counter += 1;
  return result;
```    
