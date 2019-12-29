## Problem

In DNA strings, symbols "A" and "T" are complements of each other, as "C" and "G". You have function with one side of the DNA (string, except for Haskell); you need to get the other complementary side. DNA strand is never empty or there is no DNA at all (again, except for Haskell).

### Example

* DNA_strand ("ATTGC") # return "TAACG"

* DNA_strand ("GTAT") # return "CATA"



**First Solution:**
```python
def DNA_strand(dna):
    nucleotides = list(dna.lower());
    complementary = ""
    for base in nucleotides:
      if base == "a":
        complementary += "t";
      if base == "t":
        complementary += "a";
      if base == "c":
        complementary += "g";
      if base == "g":
        complementary += "c";
    return complementary.upper();
```
