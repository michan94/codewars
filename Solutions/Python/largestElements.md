## Problem

Complete the function that returns an array of length n, starting with the given number x and the squares of the previous number. If n is negative or zero, return an empty array/list.

## Examples

2, 5 --> [2, 4, 16, 256, 65536]
3, 3 --> [3, 9, 81]

**Solution 1:**

```python
def squares(x, n):
    if n <= 0:
        return []

    result = [x]
    for i in range(n-1):
        x *= x
        result.append(x)
    return result
```

**Solution 2:**

```python
def squares(x,n):
    return [x**(2**i) for i in range(n)]
```

## Problem

Write a program that outputs the top n elements from a list.

## Example:

largest(2, [7,6,5,4,3,2,1]) => [6,7]

**Solution 1:**

```python
def largest(n,xs):
    if n > len(xs):
        return [-1]

    xs.sort()
    result = []
    for i in range(n):
        result.append(xs.pop())
    return sorted(result)
```
