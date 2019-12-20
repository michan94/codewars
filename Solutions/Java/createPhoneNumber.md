
## Problem

Write a function that accepts an array of 10 integers (between 0 and 9), that returns a string of those numbers in the form of a phone number.:

* Ex: Kata.createPhoneNumber(new int[] {1, 2, 3, 4, 5, 6, 7, 8, 9, 0}) // => returns "(123) 456-7890"

**First Solution:**
```java
public class Kata {
  public static String createPhoneNumber(int[] numbers) {
    int index = 0;
    String phoneNum = "(";
    while (index < 3) {
      if (index == 2) {
        phoneNum = phoneNum + String.valueOf(numbers[index]) + ") ";
        index++;
      }
      else {
        phoneNum = phoneNum + String.valueOf(numbers[index]);
        index++;
      }
    }
    while (index > 2 && index < numbers.length) {
      if (index == 5) {
        phoneNum = phoneNum + String.valueOf(numbers[index]) + "-";
        index++;
      }
      else {
        phoneNum = phoneNum + String.valueOf(numbers[index]);
        index++;
      }
    }
    return phoneNum;
  }
}
```

