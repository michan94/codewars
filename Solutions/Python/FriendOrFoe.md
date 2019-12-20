## Problem

Make a program that filters a list of strings and returns a list with only your friends name in it.

If a name has exactly 4 letters in it, you can be sure that it has to be a friend of yours! Otherwise, you can be sure he's not...

* Ex: Input = ["Ryan", "Kieran", "Jason", "Yous"], Output = ["Ryan", "Yous"]

**First Solution:**
```python
def friend(x):
    for person in x:
        name = list(person);
        if len(name) != 4:
            x.remove(person);
    return x;
```