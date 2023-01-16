## Problem

Create a function that converts US dollars (USD) to Chinese Yuan (CNY) . The input is the amount of USD as an integer, and the output should be a string that states the amount of Yuan followed by 'Chinese Yuan'

## Examples

15 -> '101.25 Chinese Yuan'
465 -> '3138.75 Chinese Yuan'
The conversion rate you should use is 6.75 CNY for every 1 USD. All numbers should be represented as a string with 2 decimal places. (e.g. "21.00" NOT "21.0" or "21")

**Solution 1:**

```python
from decimal import Decimal

def usdcny(usd):
    return f"{Decimal(usd)*Decimal(6.75)} Chinese Yuan"
```

**Solution 2:**

```python
def usdcny(usd):
    return f"{(usd * 6.75):.2f} Chinese Yuan"
```
