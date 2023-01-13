## Problem

Several people are standing in a row divided into two teams.
The first person goes into team 1, the second goes into team 2, the third goes into team 1, and so on.

Given an array of positive integers (the weights of the people), return a new array/tuple of two integers, where the first one is the total weight of team 1, and the second one is the total weight of team 2.

Notes
Array size is at least 1.
All numbers will be positive.

## Examples

rowWeights([13, 27, 49]) ==> return (62, 27)
rowWeights([50, 60, 70, 80]) ==> return (120, 140)
rowWeights([80]) ==> return (80, 0)

**First Solution:**

```python
def row_weights(array):
    if len(array) < 2:
        return (array[0],0)

    first = second = 0
    for i in range(len(array)):
        if i % 2 == 0:
            first += array[i]
        else:
            second += array[i]
    return (first, second)
```

**Second Solution:**

```python
def row_weights(array):
    return sum(array[::2]), sum(array[1::2])
```
