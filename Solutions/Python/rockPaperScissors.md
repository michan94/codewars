## Problem

Let's play! You have to return which player won! In case of a draw return Draw!.

### Examples:

rps('scissors','paper') // Player 1 won!
rps('scissors','rock') // Player 2 won!
rps('paper','paper') // Draw!



**First Solution:**
```python
def rps(p1, p2):
  if p1 == "scissors" and p2 == "paper":
    return "Player 1 won!"
  elif p1 == "paper" and p2 == "scissors":
    return "Player 2 won!"
  
  if p1 == "rock" and p2 == "scissors":
    return "Player 1 won!"
  elif p1 == "scissors" and p2 == "rock":
    return "Player 2 won!"
  
  if p1 == "paper" and p2 == "rock":
    return "Player 1 won!"
  elif p1 == "rock" and p2 == "paper":
    return "Player 2 won!"
    
  else:
    return "Draw!"
```