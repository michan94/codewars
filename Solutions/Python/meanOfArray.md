## Problem

It's the academic year's end, fateful moment of your school report. The averages must be calculated. All the students come to you and entreat you to calculate their average for them. Easy ! You just need to write a script.

Return the average of the given array rounded down to its nearest integer.

The array will never be empty.

**First Solution:**

```python
def get_average(marks):
    return sum(marks)//len(marks)
```

**Second Solution:**

```python
def get_average(marks):
    total = 0
    for mark in marks:
        total += mark
    return total // len(marks)
```
