## Problem

Complete the solution so that the function will break up camel casing, using a space between words.

Example
"camelCasing" => "camel Casing"
"identifier" => "identifier"
"" => ""

**First Solution:**

```python
def solution(s):
    result = ''
    for letter in s:
        if letter != letter.upper():
            result += letter
        else:
            result += f" {letter.upper()}"
    return result
```
