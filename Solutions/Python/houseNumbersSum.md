## Problem

A boy is walking a long way from school to his home. To make the walk more fun he decides to add up all the numbers of the houses that he passes by during his walk. Unfortunately, not all of the houses have numbers written on them, and on top of that the boy is regularly taking turns to change streets, so the numbers don't appear to him in any particular order.

At some point during the walk the boy encounters a house with number 0 written on it, which surprises him so much that he stops adding numbers to his total right after seeing that house.

For the given sequence of houses determine the sum that the boy will get. It is guaranteed that there will always be at least one 0 house on the path.

### Example

*  inputArray = [5, 1, 2, 3, 0, 1, 5, 0, 2], the output should be 11


**First Solution:**
```python
def house_numbers_sum(inp):
  total = 0;
  for house in inp:
    if house != 0:
      total += house;
    if house == 0:
      return total;
  return total; 
```
