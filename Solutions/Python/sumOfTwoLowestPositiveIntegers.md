## Problem

Create a function that returns the sum of the two lowest positive numbers given an array of minimum 4 positive integers. No floats or non-positive integers will be passed.

### Example

* When an array is passed like [19, 5, 42, 2, 77], the output should be 7.

* [10, 343445353, 3453445, 3453545353453] should return 3453455.



**First Solution:**
```python
def sum_two_smallest_numbers(numbers):
  sum = 0;
  nums = numbers.sort();
  nums = numbers[0:2];
  for num in nums:
    sum += num;
  return sum;
```
