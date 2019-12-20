
## Problem

You are given an array (which will have a length of at least 3, but could be very large) containing integers. The array is either entirely comprised of odd integers or entirely comprised of even integers except for a single integer N. Write a method that takes the array as an argument and returns this "outlier" N.

* Example:
* [2, 4, 0, 100, 4, 11, 2602, 36]
Should return: 11 (the only odd number)
* [160, 3, 1719, 19, 11, 13, -21]
Should return: 160 (the only even number)

**First Solution:**
```java
public class FindOutlier{
  static int find(int[] integers){
  int evenCount = 0;
  int oddCount = 0;
  int outlier = 0;
  for (int i=0; i<3; i++) {				//Find if list if even or odd majority
    if (integers[i] % 2 == 0) {
      evenCount++;
    }
    else {
      oddCount++;
    }
  }
  
  if (evenCount > 1) {					// Start finding the odd number
  	for (int j=0; j < integers.length; j++) {
  		if (integers[j] % 2 != 0) {
 			outlier = integers[j]; 		
  		}
  	}		
  }
  else {								//Start finding the even number
  	for (int k=0; k <integers.length; k++) {
  		if (integers[k] % 2 == 0) {
  			outlier = integers[k];
  		}
  	}
  }
  return outlier;
}
}

```

