# Problem 2.3: Mobile to Tree (200pts)

Implement `totals_tree`, which takes a mobile (or planet) and returns a tree whose root is the total weight of the input. For a planet, the result should be a leaf. For a mobile, the result should be a tree and its branches should be the `totals_tree` for each ends of the arms.

```python
from ADT import tree, label, branches, is_leaf, print_tree

def totals_tree(m):
    """Return a tree representing the mobile/planet with its total weight at the root.

    >>> t, u, v = examples()
    >>> print_tree(totals_tree(t))
    3
      2
      1
    >>> print_tree(totals_tree(u))
    6
      1
      5
        3
        2
    >>> print_tree(totals_tree(v))
    9
      3
        2
        1
      6
        1
        5
          3
          2
    """
    assert is_mobile(m) or is_planet(m)
    "*** YOUR CODE HERE ***"

```

> _Hint_: you may want to use some helper functions imported from ADT.py.
