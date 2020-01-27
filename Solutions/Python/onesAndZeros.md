## Problem

Given an array of ones and zeroes, convert the equivalent binary value to an integer.

Eg: [0, 0, 0, 1] is treated as 0001 which is the binary representation of 1.

### Examples:

Testing: [0, 0, 0, 1] ==> 1

Testing: [0, 0, 1, 0] ==> 2

Testing: [0, 1, 0, 1] ==> 5

Testing: [1, 0, 0, 1] ==> 9

Testing: [0, 0, 1, 0] ==> 2

Testing: [0, 1, 1, 0] ==> 6

Testing: [1, 1, 1, 1] ==> 15

Testing: [1, 0, 1, 1] ==> 11

However, the arrays can have varying lengths, not just limited to 4.



**First Solution:**
```python
def binary_array_to_number(arr):
  result = 0;
  counter = 0;
  for digit in arr[::-1]:
    if digit == 1:
      if counter == 0:
        result += 1;
        counter += 1;
      else:
        result += (2 ** counter);
        counter += 1;
    if digit == 0:
      counter += 1;
      continue;
  return result;
```