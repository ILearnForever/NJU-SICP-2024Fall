# Problem 1: Take While (100pts)

Implement `takeWhile`, which takes in an iterator `t` and a predicate `p`. `takeWhile` yields the values from `t` up to the first element that does not satisfy `p`.

A predicate `p` is just a pure function with one argument and returns either `True` or `False`.

```python
def takeWhile(t, p):
    """Take elements from t until p is not satisfied.

    >>> s = iter([10, 9, 10, 9, 9, 10, 8, 8, 8, 7])
    >>> list(takeWhile(s, lambda x: x == 10))
    [10]
    >>> s2 = iter([1, 1, 2, 3, 5, 8, 13])
    >>> list(takeWhile(s2, lambda x: x % 2 == 1))
    [1, 1]
    >>> s = iter(['a', '', 'b', '', 'c'])
    >>> list(takeWhile(s, lambda x: x != ''))
    ['a']
    >>> list(takeWhile(s, lambda x: x != ''))
    ['b']
    >>> next(s)
    'c'
    """
    "*** YOUR CODE HERE ***"
```

\
