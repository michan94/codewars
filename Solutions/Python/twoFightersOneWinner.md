## Problem

Create a function that returns the name of the winner in a fight between two fighters.

Each fighter takes turns attacking the other and whoever kills the other first is victorious. Death is defined as having health <= 0.

Each fighter will be a Fighter object/instance. See the Fighter class below in your chosen language.

Both health and damagePerAttack (damage_per_attack for python) will be integers larger than 0. You can mutate the Fighter objects.

### Example

* declare_winner(Fighter("Lew", 10, 2),Fighter("Harry", 5, 4), "Lew"), "Lew")

* Fighter("Lew", 10, 2),Fighter("Harry", 5, 4), "Harry"),"Harry")

* Fighter("Harald", 20, 5), Fighter("Harry", 5, 4), "Harry"),"Harald")



**First Solution:**
```python
def declare_winner(fighter1, fighter2, first_attacker):
  while fighter1.health > 0 and fighter2.health > 0:
    if first_attacker == fighter1:
      while fighter1.health > 0 or fighter2.health > 0:
        fighter2.health -= fighter1.damage_per_attack;
        if fighter2.health <= 0:
          return fighter1.name;
        fighter1.health -= fighter2.damage_per_attack;
        if fighter1.health <= 0:
          return fighter2.name;
    else:
      while fighter1.health > 0 or fighter2.health > 0:
        fighter1.health -= fighter2.damage_per_attack;
        if fighter1.health <= 0:
          return fighter2.name;
        fighter2.health -= fighter1.damage_per_attack;
        if fighter2.health <= 0:
          return fighter1.name;
```
