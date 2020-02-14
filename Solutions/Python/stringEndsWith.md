## Problem

Complete the solution so that it returns true if the first argument(string) passed in ends with the 2nd argument (also a string).

### Examples:

solution('abc', 'bc') # returns true

solution('abc', 'd') # returns false

**First Solution:**
```python
def solution(string, ending):
	return string.endswith(ending);
```

**Second Solution:**
```python
def solution(string, ending):
  lenCompare = len(string) - len(ending)
  string3 = string[lenCompare:]
  if string3 == ending:
    return True
  else:
    return False
```