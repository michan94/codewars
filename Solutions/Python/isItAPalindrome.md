## Problem

Write function isPalindrome that checks if a given string (case insensitive) is a palindrome.

In Racket, the function is called palindrome?

(palindrome? "nope") ; returns #f

(palindrome? "Yay")  ; returns #t

**First Solution:**
```python
def is_palindrome(s):
  palindrome = False;
  s = list(s.lower());
  reverse = s[::-1];
  if s == reverse:
    palindrome = True;
#  print(s);
#  print(reverse);
  return palindrome;
```    
