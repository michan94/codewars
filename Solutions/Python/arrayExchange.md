## Problem

Array Exchange and Reversing

It's time for some array exchange! The objective is simple: exchange the elements of two arrays in-place in a way that their new content is also reversed.

### Before

my_list = ['a', 'b', 'c']

other_list = [1, 2, 3]

exchange_with(my_list, other_list)

### After

my_list == [3, 2, 1]

other_list == ['c', 'b', 'a']

**First Solution:**
```python
def exchange_with(a, b):
  revA = [];
  revB = [];
  for item in a[::-1]:
    revA.append(item);
    a.remove(item);
  for item in b[::-1]:
    revB.append(item);
    b.remove(item);
  for item in revA:
    b.append(item);
  for item in revB:
    a.append(item);
```