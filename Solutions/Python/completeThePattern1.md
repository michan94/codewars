## Problem

You have to write a function pattern which returns the following Pattern(See Pattern & Examples) upto n number of rows.

If n < 1 then it should return "" i.e. empty string.

1

22

333

....

.....

nnnnnn

### Examples:

pattern(5):

1

22

333

4444

55555

pattern(11):

1

22

333

4444

55555

666666

7777777

88888888

999999999

10101010101010101010

1111111111111111111111


**First Solution:**
```python
def pattern(n):
  result = "1";
  if n < 1:
    return "";
  else:
    for i in range(2, n+1):
      result += "\n";
      count = i;
      while count > 0:
        result += str(i);
        count -= 1;
  return result;
```
