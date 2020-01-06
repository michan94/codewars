## Problem

write me a function stringy that takes a size and returns a string of alternating '1s' and '0s'.

the string should start with a 1.

The size will always be positive and will only use whole numbers

### Example

* a string with size 6 should return :'101010'.

* with size 4 should return : '1010'.

* with size 12 should return : '101010101010'.


**First Solution:**
```java
public class Kata {
  public static String stringy(int size) {
    String output = "1";
    if (size == 1) {
      return output;
    }
    else {
      for (int i = 0; i < size-1; i++) {
        if (i % 2 != 0) {
          output += "1";
        }
        else {
          output += "0";
        }
      }
    }
    return output;
  }
}
```
