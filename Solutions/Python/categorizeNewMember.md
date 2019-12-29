## Problem

The Western Suburbs Croquet Club has two categories of membership, Senior and Open. They would like your help with an application form that will tell prospective members which category they will be placed.

To be a senior, a member must be at least 55 years old and have a handicap greater than 7. In this croquet club, handicaps range from -2 to +26; the better the player the lower the handicap.

Input will consist of a list of lists containing two items each. Each list contains information for a single potential member. Information consists of an integer for the person's age and an integer for the person's handicap.

Output will consist of a list of string values (in Haskell: Open or Senior) stating whether the respective member is to be placed in the senior or open category.

### Example

* openOrSenior([[45, 12],[55,21],[19, -2],[104, 20]]),['Open', 'Senior', 'Open', 'Senior']

* openOrSenior([[16, 23],[73,1],[56, 20],[1, -1]]),['Open', 'Open', 'Senior', 'Open']



**First Solution:**
```python
def openOrSenior(data):
  placements = [];
  data = list(data);
  for member in data:
    if member[0] >= 55:  
      if member[1] in range(8, 27):
        placements.append("Senior");
      if member[1] in range (-2, 8):
        placements.append("Open");
    else:  
      placements.append("Open");
  return placements;
```