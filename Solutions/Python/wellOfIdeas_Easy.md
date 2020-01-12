## Problem

For every good kata idea there seem to be quite a few bad ones!

In this kata you need to check the provided array (x) for good ideas 'good' and bad ideas 'bad'. If there are one or two good ideas, return 'Publish!', if there are more than 2 return 'I smell a series!'. If there are no good ideas, as is often the case, return 'Fail!'.


**First Solution:**
```python
import string

def is_pangram(s):
    pangram = False;
    usedLetters = list("abcdefghijklmnopqrstuvwxyz");
    sentence = s.lower();
    for letter in sentence:
      if letter.isalpha():
        if letter in usedLetters:
          usedLetters.remove(letter);
    if len(usedLetters) == 0:
      pangram = True;
    return pangram;            #or return len(usedLetters)==26
    
    
    
    #have array of valid letters
    #go through each letter of sentence --> list(s)
    #once a letter is found, if it is still in validLetters, delete it
    #when finish for-loop, if validLetters still has a value, return False

```