## Problem

Given two integers a and b, which can be positive or negative, find the sum of all the numbers between including them too and return it. If the two numbers are equal return a or b.

Note: a and b are not ordered!

### Example

*  GetSum(1, 0) == 1   // 1 + 0 = 1

* GetSum(1, 2) == 3   // 1 + 2 = 3

* GetSum(0, 1) == 1   // 0 + 1 = 1

* GetSum(1, 1) == 1   // 1 Since both are same

* GetSum(-1, 0) == -1 // -1 + 0 = -1

* GetSum(-1, 2) == 2  // -1 + 0 + 1 + 2 = 2


**First Solution:**
```java
public class Sum {
  public int GetSum(int a, int b) {
    int total = 0;
    if (a == b) {
      total = a;
    }
    else if (a > b) {
      for (int i = b; i <= a; i++) {
        total += i;
      }
    }
    else if (b > a) {
      for (int j = a; j <= b; j++) {
        total += j;
      }
    }
    return total; 
  }
}
```
