## Problem

When provided with a number between 0-9, return it in words.

Input :: 1

Output :: "One".

**First Solution:**

```python
def switch_it_up(number):
    stringNum = {0:'Zero',1:'One',2:'Two',3:'Three',4:'Four',5:'Five',6:'Six',7:'Seven',8:'Eight',9:'Nine',}
    return stringNum[number]
```
