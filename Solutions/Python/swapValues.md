## Problem

I would like to be able to pass an array with two elements to my swapValues function to swap the values. However it appears that the values aren't changing.

Can you figure out what's wrong here?

**Initial Code:**
```python
def swap_values(args):
  args[0] = args[1]
  args[1] = args[0];
```

**First Solution:**
```python
def swap_values(args): 
  swap = args[0]
  args[0] = args[1]
  args[1] = swap;
```