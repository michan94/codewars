## Problem

Everybody knows a little german, right? But remembering the correct articles is a tough job. Write yourself a little helper, that returns the noun with the matching article:

each noun containing less than 2 vowels has the article "das"
each noun containing 2/3 vowels has the article "die"
each noun containing more than 3 vowels has the article "der"
Caution: Vowels are "a,e,i,o,u". Umlaute (ä ö ü) are also being counted!

**First Solution:**

```python
def der_die_das(wort):
    vowels = ['a','e','i','o','u','ä','ö','ü']
    numVowels = 0
    for letter in wort.lower():
        if letter in vowels:
            numVowels += 1
    if numVowels < 2:
        return 'das ' + wort
    elif numVowels < 4:
        return 'die ' + wort
    else:
        return 'der ' + wort
```
