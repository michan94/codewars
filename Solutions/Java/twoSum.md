## Problem

Write a function that takes an array of numbers (integers for the tests) and a target number. It should find two different items in the array that, when added together, give the target value. The indices of these items should then be returned in a tuple like so: (index1, index2).

For the purposes of this kata, some tests may have multiple answers; any valid solutions will be accepted.

The input will always be valid (numbers will be an array of length 2 or greater, and all of the items will be numbers; target will always be the sum of two different items from that array).

### Example

* twoSum [1, 2, 3] 4 === (0, 2)


**First Solution:**
```java
public class Solution {
    public static int[] twoSum(int[] numbers, int target) {
      int size = numbers.length;
      int[] result = new int[2];
      if (size < 2) {          //Assume instructions didn't say that input would always be valid
        return new int[] {-1, -1};
      }
      else {
        for (int i = 0; i < size - 1; i++) {
          for (int j = i + 1; j < size; j++) {
            if ((target - numbers[i]) == numbers[j]) {
              result[0] = i;
              result[1] = j;
            }
          }
        }
      }
      return result;
    }
}
```


**Second Solution:**
```java
import java.util.HashMap;

public class Solution {
  public static int[] twoSum(int[] numbers, int target) {    //Saw HashMap Solution so thought I'd attempt to implement
    int size = numbers.length;
    HashMap<Integer, Integer> holder = new HashMap<Integer, Integer>();
    int[] result = new int[2];
    if (size < 2) {
      return null;
    }
    for (int i = 0; i < size; i++) {
      if (holder.containsKey(target - numbers[i])) {
        result[0] = i;
        result[1] = holder.get(target - numbers[i]);
      }
      else {
        holder.put(numbers[i], i);    // [value, index]
      }
    }
    return result;
  }
}
```
