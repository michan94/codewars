## Problem

Timmy & Sarah think they are in love, but around where they live, they will only know once they pick a flower each. If one of the flowers has an even number of petals and the other has an odd number of petals it means they are in love.

Write a function that will take the number of petals of each flower and return true if they are in love and false if they aren't.

**First Solution:**
```java
public class OppositesAttract {

  public static boolean isLove(final int flower1, final int flower2) {
    boolean inLove = false;
    boolean petals1, petals2;
    petals1 = (flower1 % 2) == 0;
    petals2 = (flower2 % 2) == 0;
    if (petals1 != petals2) {
      inLove = true;
    }
    return inLove;
  }  
} 
```
