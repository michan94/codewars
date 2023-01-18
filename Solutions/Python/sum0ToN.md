## Problem

We want to generate a function that computes the series starting from 0 and ending until the given number.

## Examples

Input:

> 6
> Output:
> 0+1+2+3+4+5+6 = 21

Input:

> -15
> Output:
> -15<0

Input:

> 0
> Output:

0=0

**Solution 1:**

```python
def show_sequence(n):
    if n < 0:
        return f"{n}<0"
    if n == 0:
        return f"{n}=0"

    result = ''
    for i in range(n+1):
        result += f"{i}+"
    return f"{result[:-1]} = {sum(range(0,n+1))}"
```

**Solution 2:**

```python
def show_sequence(n):
    if n < 0:
        return f"{n}<0"
    if n == 0:
        return f"{n}=0"

    result = ''
    total = 0
    for i in range(n+1):
        result += f"{i}+"
        total += i
    return f"{result[:-1]} = {total}"
```
