# Problem 1: F91 (100pts)

The f91 function is a recursive function, defined by the computer scientist [John McCarthy](https://en.wikipedia.org/wiki/John_McCarthy_\(computer_scientist\)) as a test case for formal verification within computer science.

Write a recursive function `f91` that takes a single argument n,

* returns `n - 10` when `n > 100`
* returns `f91(f91(n + 11))` when `n ≤ 100`

```python
def f91(n):
    """Takes a number n and returns n - 10 when n > 100,
    returns f91(f91(n + 11)) when n ≤ 100.

    >>> f91(1)
    91
    >>> f91(2)
    91
    >>> f91(100)
    91
    """
    "*** YOUR CODE HERE ***"

```

> Q: It seems that the argument of `f91`'s recursive calls is not always **simpler** in terms of less-than relation of integers.
>
> A: Oh, the meaning of "**simpler**" is not that simple ...
