## Problem

You're writing code to control your town's traffic lights. You need a function to handle each change from green, to yellow, to red, and then to green again.

Complete the function that takes a string as an argument representing the current state of the light and returns a string representing the state the light should change to.

For example, when the input is green, output should be yellow.

**Problem 1:**

```python
def update_light(current):
    nextLight = {'green':'yellow','yellow':'red','red':'green'}
    return nextLight[current]
```
