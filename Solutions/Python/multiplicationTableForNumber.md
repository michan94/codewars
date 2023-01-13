## Problem

Your goal is to return multiplication table for number that is always an integer from 1 to 10.

For example, a multiplication table (string) for number == 5 looks like below:

## Examples

1 _ 5 = 5
2 _ 5 = 10
3 _ 5 = 15
4 _ 5 = 20
5 _ 5 = 25
6 _ 5 = 30
7 _ 5 = 35
8 _ 5 = 40
9 _ 5 = 45
10 _ 5 = 50

P. S. You can use \n in string to jump to the next line.

Note: newlines should be added between rows, but there should be no trailing newline at the end. If you're unsure about the format, look at the sample tests.

**First Solution:**

```python
def multi_table(number):
    result = ''
    for i in range(1,11):
        result += f'{i} * {number} = {number * i}\n'
    return result[:-1]
```
