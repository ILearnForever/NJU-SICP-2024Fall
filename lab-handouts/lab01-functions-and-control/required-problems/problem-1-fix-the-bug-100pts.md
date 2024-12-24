# Problem 1: Fix the Bug (100pts)

The following snippet of code doesn't work as expected! Figure out what is wrong and **fix the bug**.

```python
def both_odd(a, b):
    """Returns True if both a and b are odd numbers.

    >>> both_odd(-1, 1)
    True
    >>> both_odd(2, 1)
    False
    """
    return a and b % 2 == 1 # You can replace this line!
```

> Test your implementation with `python ok -q both_odd`.
