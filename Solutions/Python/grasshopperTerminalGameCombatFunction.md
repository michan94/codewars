## Problem

Create a combat function that takes the player's current health and the amount of damage recieved, and returns the player's new health. Health can't be less than 0.

**First Solution:**
```python
def combat(health, damage):
  after = health - damage;
  if after < 0:
    return 0;
  return after;
```    
