## Problem

Middle Earth is about to go to war. The forces of good will have many battles with the forces of evil. Different races will certainly be involved. Each race has a certain worth when battling against others.

On the side of good we have the following races, with their associated worth:

Hobbits: 1
Men: 2
Elves: 3
Dwarves: 3
Eagles: 4
Wizards: 10

On the side of evil we have:

Orcs: 1
Men: 2
Wargs: 2
Goblins: 2
Uruk Hai: 3
Trolls: 5
Wizards: 10

Given the count of each of the races on the side of good, followed by the count of each of the races on the side of evil, determine which side wins.

Input:
The function will be given two parameters. Each parameter will be a string of multiple integers separated by a single space. Each string will contain the count of each race on the side of good and evil.

The first parameter will contain the count of each race on the side of good in the following order:

Hobbits, Men, Elves, Dwarves, Eagles, Wizards.
The second parameter will contain the count of each race on the side of evil in the following order:

Orcs, Men, Wargs, Goblins, Uruk Hai, Trolls, Wizards.
All values are non-negative integers. The resulting sum of the worth for each side will not exceed the limit of a 32-bit integer.

Output:
Return "Battle Result: Good triumphs over Evil" if good wins, "Battle Result: Evil eradicates all trace of Good" if evil wins, or "Battle Result: No victor on this battle field" if it ends in a tie.

**Solution 1:**

```python
def good_vs_evil(good, evil):
    goodArmy, evilArmy = good.split(), evil.split()
    for i in range(len(goodArmy)):
        if i in range(1):
            goodArmy[i] = int(goodArmy[i])
        elif i in range(1,2):
            goodArmy[i] = int(goodArmy[i]) * 2
        elif i in range(2,4):
            goodArmy[i] = int(goodArmy[i]) * 3
        elif i in range(4,5):
            goodArmy[i] = int(goodArmy[i]) * 4
        else:
            goodArmy[i] = int(goodArmy[i]) * 10
    for i in range(len(evilArmy)):
        if i in range(1):
            evilArmy[i] = int(evilArmy[i])
        elif i in range(1,4):
            evilArmy[i] = int(evilArmy[i]) * 2
        elif i in range(4,5):
            evilArmy[i] = int(evilArmy[i]) * 3
        elif i in range(5,6):
            evilArmy[i] = int(evilArmy[i]) * 5
        else:
            evilArmy[i] = int(evilArmy[i]) * 10
    if sum(goodArmy) > sum(evilArmy):
        return f'Battle Result: Good triumphs over Evil'
    elif sum(goodArmy) < sum(evilArmy):
        return f'Battle Result: Evil eradicates all trace of Good'
    return f'Battle Result: No victor on this battle field'
```
