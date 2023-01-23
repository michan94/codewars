## Problem

Complete function saleHotdogs/SaleHotDogs/sale_hotdogs, function accepts 1 parameter:n, n is the number of hotdogs a customer will buy, different numbers have different prices (refer to the following table), return how much money will the customer spend to buy that number of hotdogs.

**Solution 1:**

```python
def sale_hotdogs(n):
    if n < 5:
        return 100 * n
    if n >= 5 and n < 10:
        return 95 * n
    return 90 * n
```
