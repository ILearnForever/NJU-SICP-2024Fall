# Problem 3: Deep (50pts)

When nested mutable objects appear, the behavior of your program might be confusing. Consider the example below

```python
>>> inner1 = [1, 2, 3]
>>> inner2 = [4, 5, 6]
>>> a = [inner1, inner2]
>>> a
[[1, 2, 3], [4, 5, 6]]
>>> b1 = a
>>> b2 = a[:]
>>> b3 = [a[0][:], a[1][:]]
>>> b1 == b2 and b2 == b3 and b1 == b3
True
>>> inner1[0] = 222
>>> b1
[[222, 2, 3], [4, 5, 6]]
>>> b2
[[222, 2, 3], [4, 5, 6]]
>>> b3
[[1, 2, 3], [4, 5, 6]]
```

1. We call `b1` an alias of `a`, since they are just different names for the same list.
2. We call `b2` a _shallow-copy_ of `a`, which means `b2` is not `a`, but the contents of `b2` are the same objects as the contents of `a`.
3. We call `b3` a _deep-copy_ of `a`, as all the contents of `b3` (i.e., lists of integers) are created via slicing and are not the same objects as the contents of `a`.

Now you need to implement a function `deep` to create a _deep-copy_ of a given non-empty list, whose contents are non-empty lists of integers. In the real-world, objects may be arbitrarily nested (e.g., lists of lists of lists of ...), but in this problem, you only need to handle a simple situation, where the contents of the given list are only lists of integers.

> _Hint_: try to use list comprehension to make your answer concise

```python
def deep(l):
    """Returns a deep-copy of the given list of lists.
    >>> a = [[2, 2, 2], [5, 0, 2], [5, 0, 3]]
    >>> b = deep(a)
    >>> b
    [[2, 2, 2], [5, 0, 2], [5, 0, 3]]
    >>> a is b
    False
    >>> a[0] is b[0]
    False
    >>> a[1] is b[1]
    False
    >>> a[2] is b[2]
    False
    >>> len(a) == len(b)
    True
    """
    "*** YOUR CODE HERE ***"
```
