## Problem

ATM machines allow 4 or 6 digit PIN codes and PIN codes cannot contain anything but exactly 4 digits or exactly 6 digits.

If the function is passed a valid PIN string, return true, else return false.

### Ex: 

* validate_pin("1234") == True

* validate_pin("12345") == False

* validate_pin("a234") == False

**First Solution:**
```python
def validate_pin(pin):
  validNums = "0123456789";
  validNumsList = list(validNums);
  pin = list(pin);
  valid = True;
  if (len(pin) != 4) and (len(pin) != 6):
    valid = False;
  else:
    for digit in pin:
      if digit not in validNumsList:
        valid = False;
  return valid;       
```
