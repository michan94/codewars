## Problem

The following code is not giving the expected results. Can you debug what the issue is?

The following is an example of data that would be passed in to the function.

data = [
{'name': 'Joe', 'age': 20},
{'name': 'Bill', 'age': 30},
{'name': 'Kate', 'age': 23}
]
get_names(data) # should return ['Joe', 'Bill', 'Kate']

**Solution 1:**

```python
def itemgetter(item):
    return item['name']

def get_names(data):
    return list(map(itemgetter, data))
```
