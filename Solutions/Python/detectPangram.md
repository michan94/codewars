## Problem

A pangram is a sentence that contains every single letter of the alphabet at least once. For example, the sentence "The quick brown fox jumps over the lazy dog" is a pangram, because it uses the letters A-Z at least once (case is irrelevant).

Given a string, detect whether or not it is a pangram. Return True if it is, False if not. Ignore numbers and punctuation.

### Example

* pangram = "The quick, brown fox jumps over the lazy dog!"

Test.assert_equals(is_pangram(pangram), True)



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