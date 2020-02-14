## Problem

In this little assignment you are given a string of space separated numbers, and have to return the highest and lowest number.

### Example:

high_and_low("1 2 3 4 5")  # return "5 1"

high_and_low("1 2 -3 4 5") # return "5 -3"

high_and_low("1 9 3 4 -5") # return "9 -5"

**First Solution:**
```python
def high_and_low(numbers):
  temp = numbers.split();
  numbersInt = [];
  for num in temp:
    numbersInt.append(int(num));
  highest = max(numbersInt);
  lowest = min(numbersInt);
  result = str(highest) + " " + str(lowest);
  return result
```

**Second Solution:**
```python
def high_and_low(numbers):
  temp = numbers.split();
  numbersInt = [];
  for num in temp:
    numbersInt.append(int(num));
  numbersInt.sort();
  highest = numbersInt[len(numbersInt)-1]
  lowest = numbersInt[0];
  result = str(highest) + " " + str(lowest);
  return result
```