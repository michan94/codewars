## Problem

Create a method is_uppercase() to see whether the string is ALL CAPS. 

### Example

* is_uppercase("c") == False

* is_uppercase("C") == True

* is_uppercase("hello I AM DONALD") == False

* is_uppercase("HELLO I AM DONALD") == True

* is_uppercase("ACSKLDFJSgSKLDFJSKLDFJ") == False

* is_uppercase("ACSKLDFJSGSKLDFJSKLDFJ") == True


**First Solution:**
```python
def is_uppercase(inp):
  upper = inp.upper();
  return inp == upper;
```