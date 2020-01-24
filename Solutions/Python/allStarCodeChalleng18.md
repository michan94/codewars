## Problem

All Star Code Challenge #18

Create a function called that accepts 2 string arguments and returns an integer of the count of occurrences the 2nd argument is found in the first one.

If no occurrences can be found, a count of 0 should be returned.

strCount('Hello', 'o') // => 1

strCount('Hello', 'l') // => 2

strCount('', 'z')      // => 0

Notes:

The first argument can be an empty string

The second string argument will always be of length 1

**First Solution:**
```python
def str_count(strng, letter):
  counter = 0;
  strng = list(strng);
  if len(strng) == 0:
    return 0;
  for chr in strng:
    if chr == letter:
      counter += 1;
  return counter; 
```