## Problem

Given an array/list [] of integers , Find the product of the k maximal numbers.

#### Notes

Array/list size is at least 3 .

Array/list's numbers Will be mixture of positives , negatives and zeros

Repetition of numbers in the array/list could occur.

#### Input >> Output Example

maxProduct ({4, 3, 5}, 2) ==>  return (20)

**First Solution:**
```python
def absent_vowel(x): 
  vowels = ["a", "e", "i", "o", "u"];
  x = list(x.lower());
  for letter in x:
    if letter in vowels:
      vowels.remove(letter);
      
  missing = vowels.pop();
  if missing == "a":
    return 0;
  if missing == "e":
    return 1;
  if missing == "i":
    return 2;
  if missing == "o":
    return 3;
  if missing == "u":
    return 4;
```

**Second Solution:**
```python
def absent_vowel(x): 
  vowels = ["a", "e", "i", "o", "u"];
  vowelValues = {"a" : 0, "e" : 1, "i" : 2, "o" : 3, "u" : 4};
  x = list(x.lower());
  for letter in x:
    if letter in vowels:
      vowels.remove(letter);
      
  missing = vowels.pop();
  return vowelValues.get(missing);
```