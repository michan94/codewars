## Problem

Character recognition software is widely used to digitise printed texts. Thus the texts can be edited, searched and stored on a computer.

When documents (especially pretty old ones written with a typewriter), are digitised character recognition softwares often make mistakes.

Your task is correct the errors in the digitised text. You only have to handle the following mistakes:

S is misinterpreted as 5

O is misinterpreted as 0

I is misinterpreted as 1

The test cases contain numbers only by mistake.

### Example

* Correct.correct("1F-RUDYARD K1PL1NG") ==> "IF-RUDYARD KIPLING"


**First Solution:**
```java
public class Correct {
  public static String correct(String string) {
    char[] ch = string.toCharArray();
    for (int i = 0; i < string.length(); i++) {
      if (ch[i] == '5') {
        ch[i] = 'S';
      }
      if (ch[i] == '0') {
        ch[i] = 'O';
      }
      if (ch[i] == '1') {
        ch[i] = 'I';
      }
    }
    string = String.valueOf(ch);
    return string;
  }
}
```
