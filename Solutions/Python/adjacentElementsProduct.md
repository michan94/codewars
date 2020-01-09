## Problem

Given a mixed array of number and string representations of integers, add up the string integers and subtract this from the total of the non-string integers.

Return as a number.

### Examples

* div_con([9, 3, '7', '3']) --> 2

**First Solution:**
```python
def adjacentElementsProduct(inputArray):
    finalProducts = [];
    for element in range(len(inputArray) - 1):
        finalProducts.append(inputArray[element] * inputArray[element+1]);
    finalProducts.sort();
    return finalProducts[len(finalProducts) - 1];
```
