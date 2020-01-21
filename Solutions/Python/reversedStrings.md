## Problem

Complete the solution so that it reverses the string value passed into it.

## Example

* solution('world') # returns 'dlrow'

**First Solution:**
```python
def solution(string):
  result = "";
  string = list(string);
  for letter in string[::-1]:
    result += letter;
  return result;
```    
