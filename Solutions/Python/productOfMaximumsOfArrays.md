## Problem

Given an array/list [] of integers , Find the product of the k maximal numbers.

#### Notes

Array/list size is at least 3 .

Array/list's numbers Will be mixture of positives , negatives and zeros

Repetition of numbers in the array/list could occur.

#### Input >> Output Example

maxProduct ({4, 3, 5}, 2) ==>  return (20)

**First Solution:**
```python
def max_product(lst, n_largest_elements):
  lst.sort(reverse = True);
  total = 1;
  for num in lst[0:n_largest_elements]:
    total *= num;
  return total;
```