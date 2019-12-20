
## Problem

An isogram is a word that has no repeating letters, consecutive or non-consecutive. Implement a function that determines whether a string that contains only letters is an isogram. Assume the empty string is an isogram. Ignore letter case.


* Ex: isIsogram "Dermatoglyphics" == true
* Ex: isIsogram "aba" == false
* Ex: isIsogram "moOse" == false -- ignore letter case

**First Solution:**
```java
public class isogram {
    public static boolean  isIsogram(String str) {
        str = str.toLowerCase();
        char wrd[] = str.toCharArray();
        for (int i = 0; i<str.length(); i++) {
          for (int j = i+1; j<str.length(); j++) {
            if (wrd[i] == wrd[j]) {
              return false;
            }
          }
        }
        return true;
    } 
}
```

