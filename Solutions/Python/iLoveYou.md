## Problem

Who remembers back to their time in the schoolyard, when girls would take a flower and tear its petals, saying each of the following phrases each time a petal was torn:

I love you

a little

a lot

passionately

madly

not at all

When the last petal was torn there were cries of excitement, dreams, surging thoughts and emotions.

Your goal in this kata is to determine which phrase the girls would say for a flower of a given number of petals, where nb_petals > 0

**First Solution:**
```python
def how_much_i_love_you(nb_petals):
  torn = nb_petals % 6;
  if torn == 0:
    return "not at all"
  if torn == 1:
    return "I love you";
  if torn == 2:
    return "a little";
  if torn == 3:
    return "a lot";
  if torn == 4:
    return "passionately"
  if torn == 5:
    return "madly"
```

**Second Solution:**
```python
def how_much_i_love_you(nb_petals):
  howMuch = {0 : "not at all", 1 : "I love you", 2 : "a little", 3 : "a lot", 4 : "passionately", 5 : "madly"}
  petal = nb_petals % 6;
  return howMuch.get(petal);
```
