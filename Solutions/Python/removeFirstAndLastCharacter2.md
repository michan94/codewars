## Problem

You are given a string containing a sequence of character sequences separated by commas.

Write a function which returns a new string containing the same character sequences except the first and the last ones but this time separated by spaces.

If the input string is empty or the removal of the first and last items would cause the resulting string to be empty, return an empty value (represented as a generic value NULL in the examples below).

## Examples

"1,2,3" => "2"
"1,2,3,4" => "2 3"
"1,2,3,4,5" => "2 3 4"

"" => NULL
"1" => NULL
"1,2" => NULL

**Solution 1:**

```python
def array(string):
    print(string)
    if len(string) < 5:
        return None

    elems = string.split(',')
    if len(elems) < 3:
        return None
    return ' '.join(el for el in elems[1:len(elems)-1])
```

**Solution 2:**

```python
def array(string):
    print(string)
    if len(string) < 5:
        return None

    elems = string.split(',')
    if len(elems) < 3:
        return None
    return ' '.join(el for el in elems[1:-1])
```

**Solution 3:**

```python
def array(string):
    return ' '.join(string.split(',')[1:-1]) or None
```
