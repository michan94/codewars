## Problem

Complete the function which accepts two strings and calculates the golf score of a game. Both strings will be of length 18, and each character in the string will be a number between 1 and 9 inclusive.

I have the par value for each hole on a golf course and my stroke score on each hole. I have them stored as strings, because I wrote them down on a sheet of paper. Right now, I'm using those strings to calculate my golf score by hand: take the difference between my actual score and the par of the hole, and add up the results for all 18 holes.

### Example:

If I took 7 shots on a hole where the par was 5, my score would be: 7 - 5 = 2

If I got a hole-in-one where the par was 4, my score would be: 1 - 4 = -3.


**First Solution:**
```python
def golf_score_calculator(par_string, score_string):
  score = 0;
  for i in range(len(par_string)):
    par = int(par_string[i]);
    shot = int(score_string[i]);
    score += (shot - par);
  return score;
```
