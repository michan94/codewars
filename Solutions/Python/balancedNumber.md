## Problem

A number is a Special Number if it’s digits only consist 0, 1, 2, 3, 4 or 5

Given a number determine if it special number or not .

**First Solution:**
```python
def balanced_num(number):
  number = str(number);
  print(number); 
  if len(number) == 1:
    return "Balanced";
  elif len(number) == 2:
    return "Balanced";
    
  elif len(number) % 2 != 0:    #Odd
    first = 0;
    second = 0;
    halfway = len(number) // 2;
    print(halfway);
    for digit in number[0 : halfway]:
      first += int(digit);
    for num in number[halfway + 1 : ]:
      second += int(num);
    print(first);
    print(second);
    if first == second:
      return "Balanced"
    else:
      return "Not Balanced";
      
  elif len(number) % 2 == 0:    #Even
    first = 0;
    second = 0;
    halfway = len(number) // 2;
    print(halfway);
    for digit in number[0 : halfway-1]:
      first += int(digit);
    for num in number[halfway + 1 : ]:
      second += int(num);
    print(first);
    print(second);
    if first == second:
      return "Balanced"
    else:
      return "Not Balanced";
```