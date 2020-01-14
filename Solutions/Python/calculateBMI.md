## Problem

Write function bmi that calculates body mass index (bmi = weight / height ^ 2).

if bmi <= 18.5 return "Underweight"

if bmi <= 25.0 return "Normal"

if bmi <= 30.0 return "Overweight"

if bmi > 30 return "Obese"

**First Solution:**
```python
def bmi(weight, height):
  rating = weight / (height**2);
  if rating <= 18.5:
    return "Underweight"
  if rating <= 25.0:
    return "Normal"
  if rating <= 30.0:
    return "Overweight"
  if rating > 30:
    return "Obese";
```    
