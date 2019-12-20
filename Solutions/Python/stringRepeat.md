## Problem

Write a function called repeatString which repeats the given String src exactly count times.

###Ex: 

* repeatStr(6, "I") // "IIIIII"

* repeatStr(5, "Hello") // "HelloHelloHelloHelloHello"

**First Solution:**
```python
def repeat_str(repeat, string):
    count = 0;
    result = ""
    while count < repeat:
        result += string;
        count += 1;
    return result;    
```
