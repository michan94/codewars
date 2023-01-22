## Problem

Complete the function/method so that it returns the url with anything after the anchor (#) removed.

## Examples

"www.codewars.com#about" --> "www.codewars.com"
"www.codewars.com?page=1" -->"www.codewars.com?page=1"

**Solution 1:**

```python
def remove_url_anchor(url):
    return url.partition('#')[0]
```
