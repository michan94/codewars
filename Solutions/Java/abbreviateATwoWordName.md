## Problem

Write a function to convert a name into initials. This kata strictly takes two words with one space in between them.

The output should be two capital letters with a dot separating them

### Example

* Sam Harris => S.H

* Patrick Feeney => P.F


**First Solution:**
```java
public class AbbreviateTwoWords {

  public static String abbrevName(String name) {
    String[] arrOfStr = name.split(" ");
    String firstName = arrOfStr[0].toUpperCase();
    String lastName = arrOfStr[1].toUpperCase();
    char firstInitial = firstName.charAt(0);
    char lastInitial = lastName.charAt(0);
    String initials = firstInitial + "." + lastInitial;
    return initials;
  }
}
```
