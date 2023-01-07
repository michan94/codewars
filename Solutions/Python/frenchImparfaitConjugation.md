## Problem

Given a simple French phrase, consisting of a subject and a verb in its infinitive form, you need to turn it into L'imparfait, using the table below. To conjugate a sentence in l'imparfait, drop the last two letters of the verb and replace it with the correct ending based on the subject.

Here are the endings to replace the verb with:

Subject Verb Ending
Je (I) -ais
Tu (You) -ais
Il/Elle/On (He/She/It or We) -ait
Nous (We) -ions
Vous (You or Y'all) -iez
Ils/Elles (They) -aient
Let's say you want to translate I was walking to French:

Take the subject + infinitive: Je marcher
Remove the last two letters: Je march
Apply the correct ending: Je marchais

## Examples

Je manger --> Je mangais  
Tu dormir --> Tu dormais
Elle coder --> Elle codait
Il livrer --> Il livrait
On parler --> On parlait
Nous aller --> Nous allions
Vous partir --> Vous partiez
Ils jouer --> Ils jouaient
Elles gagner --> Elles gagnaient

**First Solution:**

```python
def to_imparfait(verb_phrase):
    conjugations = {'Je':"ais",'Tu':'ais','Il':'ait','Elle':'ait','On':'ait','Nous':'ions','Vous':'iez','Ils':'aient','Elles':'aient'}
    subject = verb_phrase.split()
    result = subject[0] + ' ' + subject[1][:len(subject[1])-2] + conjugations[subject[0]]
    return result
```
