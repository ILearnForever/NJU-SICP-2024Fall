# Problem 1: Pair Abstraction (150pts)

Define function `pair` which takes in two elements and returns a function that works as a pair. You will use functions `fst` and `snd` to retrieve the values.

```python
def fst(p):
    return p(0)


def snd(p):
    return p(1)


def pair(x, y):
    """Return a function that represents a pair.

    >>> p = pair(1, 2)
    >>> fst(p)
    1
    >>> snd(p)
    2
    """
    "*** YOUR CODE HERE ***"

```

Since we have defined an abstraction composed of a constructor `pair` and two selectors `fst` and `snd`, now lets **use the abstraction** to define two functions `change_fst` and `change_snd` that modify the pair.

> Hint: You should never break the abstraction and ruin the world !

```python
def change_fst(p, v):
    """Change pair p's first element into v and return it.

    >>> p = pair(1, 2)
    >>> fst(p)
    1
    >>> snd(p)
    2
    >>> p = change_fst(p, 3)
    >>> fst(p)
    3
    >>> snd(p)
    2
    """
    "*** YOUR CODE HERE ***"


def change_snd(p, v):
    """Change pair p's second element into v and return it.

    >>> p = pair(1, 2)
    >>> fst(p)
    1
    >>> snd(p)
    2
    >>> p = change_snd(p, 3)
    >>> fst(p)
    1
    >>> snd(p)
    3
    """
    "*** YOUR CODE HERE ***"
```
