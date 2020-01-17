## Problem

Create a function, called removeVowels (or remove_vowels), that takes a string argument and returns that same string with all vowels removed (vowels are "a", "e", "i", "o", "u").

## Example

* removeVowels("drake") // => "drk"

* removeVowels("aeiou") // => ""

**First Solution:**
```python
def remove_vowels(strng):
  result = "";
  vowels = 'aeiou';
  vowels = list(vowels);
  rmv = list(strng);
  for letter in rmv:
    if letter in vowels:
      rmv.remove(letter);
  for element in rmv:
    result += element;
  return result;
```    
