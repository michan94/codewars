## Problem

Complete the function, which calculates how much you need to tip based on the total amount of the bill and the service.

You need to consider the following ratings:

Terrible: tip 0%

Poor: tip 5%

Good: tip 10%

Great: tip 15%

Excellent: tip 20%

The rating is case insensitive (so "great" = "GREAT"). If an unrecognised rating is received, then you need to return:

"Rating not recognised" in Javascript, Python and Ruby...

Because you're a nice person, you always round up the tip, regardless of the service.

### Examples

* calculate_tip(30, "poor") --> 2

**First Solution:**
```python
import math

def calculate_tip(amount, rating):
    rating = rating.lower();
    possibleRatings = ["terrible", "poor", "good", "great", "excellent"]
    if rating not in possibleRatings:
        return "Rating not recognised"
    if rating in possibleRatings:
        if (rating == "terrible"):
            return math.ceil(amount * 0);
        if (rating == "poor"):
            return math.ceil(amount * 0.05);
        if (rating == "good"):
            return math.ceil(amount * 0.1);
        if (rating == "great"):
            return math.ceil(amount * 0.15);
        else:
            return math.ceil(amount * 0.2);
```
