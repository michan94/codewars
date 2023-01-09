## Problem

The function is not returning the correct values. Can you figure out why?

Example (Input --> Output ):

3 --> "Earth"

**Original:**

```python
def get_planet_name(id):
    # This doesn't work; Fix it!
    name=""
    switch id:
        case 1: name = "Mercury"
        case 2: name = "Venus"
        case 3: name = "Earth"
        case 4: name = "Mars"
        case 5: name = "Jupiter"
        case 6: name = "Saturn"
        case 7: name = "Uranus"
        case 8: name = "Neptune"
    return name
```

**First Solution:**

```python
def get_planet_name(id):
    # This doesn't work; Fix it!
    planets = ["Mercury","Venus","Earth","Mars","Jupiter","Saturn","Uranus","Neptune"]
    return planets[id-1]
```

**Second Solution:**

```python
def get_planet_name(id):
    # This doesn't work; Fix it!
    name=""
    if id == 1:
        name = "Mercury"
    elif id == 2:
        name = "Venus"
    elif id == 3:
        name = "Earth"
    elif id == 4:
        name = "Mars"
    elif id == 5:
        name = "Jupiter"
    elif id == 6:
        name = "Saturn"
    elif id == 7:
        name = "Uranus"
    elif id == 8:
        name = "Neptune"
    return name
```

**Third Solution:**

```python
def get_planet_name(id):
    # This doesn't work; Fix it!
    if id == 1:
        return "Mercury"
    elif id == 2:
        return "Venus"
    elif id == 3:
        return "Earth"
    elif id == 4:
        return "Mars"
    elif id == 5:
        return "Jupiter"
    elif id == 6:
        return "Saturn"
    elif id == 7:
        return "Uranus"
    elif id == 8:
        return "Neptune"
```
