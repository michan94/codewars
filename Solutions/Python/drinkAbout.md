## Problem

Kids drink toddy.
Teens drink coke.
Young adults drink beer.
Adults drink whisky.
Make a function that receive age, and return what they drink.

Rules:

Children under 14 old.
Teens under 18 old.
Young under 21 old.
Adults have 21 or more.

## Examples

13 --> "drink toddy"
17 --> "drink coke"
18 --> "drink beer"
20 --> "drink beer"
30 --> "drink whisky"

**First Solution:**

```python
def people_with_age_drink(age):
    beverages = {1:'toddy',2:'coke',3:'beer',4:'whisky'}
    if age < 14:
        return f'drink {beverages[1]}'
    if age < 18:
        return f'drink {beverages[2]}'
    if age < 21:
        return f'drink {beverages[3]}'
    return f'drink {beverages[4]}'
```
