## Problem

Create a method sayHello/say_hello/SayHello that takes as input a name, city, and state to welcome a person. Note that name will be an array consisting of one or more values that should be joined together with one space between each, and the length of the name array in test cases will vary.

## Example

say_hello(['John', 'Smith'], 'Phoenix', 'Arizona')

This example will return the string --> "Hello, John Smith! Welcome to Phoenix, Arizona!"

**Solution 1:**

```python
def say_hello(name, city, state):
    return f"Hello, {' '.join(name)}! Welcome to {city}, {state}!"
```
