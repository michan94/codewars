## Problem

In this kata you will create a function that takes a list of non-negative integers and strings and returns a new list with the strings filtered out.

### Example

filter_list([1,2,'a','b']) == [1,2]

filter_list([1,'a','b',0,15]) == [1,0,15]

filter_list([1,2,'aasf','1','123',123]) == [1,2,123]



**First Solution:**
```python
def filter_list(l):
  result = [];
  l = list(l);
  for element in l:
    if element != str(element):
      result.append(element);
  return result;
```

**Second Solution:**
```python
def filter_list(l):
  result = [];
  alphabet = list("abcdefghijklmnopqrstuvwxyz");
  l = list(l);
  for element in l:
    if element not in alphabet:          #letters
      if element != str(element):        #strings
          result.append(element);
  return result;
```