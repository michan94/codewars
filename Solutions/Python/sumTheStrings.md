## Problem

Create a function that takes 2 integers in form of a string as an input, and outputs the sum (also as a string):

## Example

"4", "5" --> "9"
"34", "5" --> "39"
"", "" --> "0"
"2", "" --> "2"
"-5", "3" --> "-2"
Notes:

If either input is an empty string, consider it as zero.

Inputs and the expected output will never exceed the signed 32-bit integer limit (2^31 - 1)

**First Solution:**

```python
def sum_str(a, b):
    if not a:
        if not b:
            return '0'
        return b
    if not b:
        if not a:
            return '0'
        return a

    return str(int(a)+int(b))
```

**Second Solution:**

```python
def sum_str(a, b):
    return str(int(a or 0) + int(b or 0))
```
