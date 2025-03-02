# Problem 3.2: Big Path (100pts)

A _path_ through a tree is a list of adjacent node values that starts with the root value. Paths can end at any node but they must always go from one node to one of its branches and may not go upwards.

For example, the paths of `tree(1, [tree(2), tree(3, [tree(4), tree(5)])])` are

```
[1]
[1, 2]
[1, 3]
[1, 3, 4]
[1, 3, 5]
```

Implement `bigpath`, which takes a tree `t` and an integer `n`. It returns the number of paths in `t` whose sum is at least `n`. Assume that all node values of `t` are integers.

```python
def bigpath(t, n):
    """Return the number of paths in t that have a sum larger or equal to n.

    >>> t = tree(1, [tree(2), tree(3, [tree(4), tree(5)])])
    >>> bigpath(t, 3)
    4
    >>> bigpath(t, 6)
    2
    >>> bigpath(t, 9)
    1
    """
    "*** YOUR CODE HERE ***"
```
