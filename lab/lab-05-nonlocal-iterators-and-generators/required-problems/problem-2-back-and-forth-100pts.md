# Problem 2: Back and Forth (100pts)

Implement `backAndForth`, a generator which takes in an iterator `t` and yields elements from `t` in multiple rounds.

In round $$i$$𝑖, `backAndForth`:

1. yields consecutive $$i$$𝑖 elements from `t`, if $$i$$𝑖 is odd,
2. skips consecutive $$i$$𝑖 elements from `t`, if $$i$$𝑖 is even.

```python
def backAndForth(t):
    """Yields and skips elements from iterator t, back and forth.

    >>> list(backAndForth(iter([1, 2, 3, 4, 5, 6, 7, 8, 9])))
    [1, 4, 5, 6]
    >>> list(backAndForth(iter([1, 2, 2])))
    [1]
    >>> # generators allow us to represent infinite sequences!!!
    >>> def naturals():
    ...     i = 0
    ...     while True:
    ...         yield i
    ...         i += 1
    >>> m = backAndForth(naturals())
    >>> [next(m) for _ in range(9)]
    [0, 3, 4, 5, 10, 11, 12, 13, 14]
    """
    "*** YOUR CODE HERE ***"
```
