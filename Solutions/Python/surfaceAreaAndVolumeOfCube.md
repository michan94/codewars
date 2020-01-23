## Problem

Write a function that returns the total surface area and volume of a box as an array: [area, volume]


**First Solution:**
```python
def get_size(w,h,d):
  result = [];
  surfaceArea = (2 * (w * h)) + (2 * (w * d)) + (2 * (h * d));
  volume = w * h * d;
  result.append(surfaceArea);
  result.append(volume);
  return result;
```    
