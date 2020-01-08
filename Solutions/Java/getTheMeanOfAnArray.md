## Problem

It's the academic year's end, fateful moment of your school report. The averages must be calculated. All the students come to you and entreat you to calculate their average for them. Easy ! You just need to write a script.

Return the average of the given array rounded down to its nearest integer.

The array will never be empty.

**First Solution:**
```java
public class School{

 	public static int getAverage(int[] marks){
    int numCourses = marks.length;
    int totalGrade = 0;
    for (int i = 0; i < numCourses; i++) {
      totalGrade += marks[i];
    }
	int avg = totalGrade / numCourses;
    return avg;
	}
}
```
