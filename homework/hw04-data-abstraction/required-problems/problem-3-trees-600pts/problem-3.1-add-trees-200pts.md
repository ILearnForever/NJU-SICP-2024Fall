# Problem 3.1: Add trees (200pts)

Define the function `add_trees`, which takes in two trees and returns a new tree where each corresponding node from the first tree is added with the node from the second tree. If a node at any particular position is present in one tree but not the other, it should be present in the new tree as well.

> _Hint_：
>
> 1. `label(t)` may not be a number.
> 2. _returns a new tree_ means that you should call the `tree` constructor for every nodes of the returned tree.
> 3. Do not modify the given trees or reuse branches directly from the given trees, call `tree` constructors instead.
> 4. Do not simply call `list(branches(t))` to copy the branches of a tree `t`, as it creates a _shallow-copy_ instead of a _deep-copy_ of the list.
> 5. You may want to use `copy_tree` defined in `ADT.py` to **deep-copy** a tree.

```python
def add_trees(t1, t2):
    """
    >>> numbers = tree(1,
    ...                [tree(2,
    ...                      [tree(3),
    ...                       tree(4)]),
    ...                 tree(5,
    ...                      [tree(6,
    ...                            [tree(7)]),
    ...                       tree(8)])])
    >>> print_tree(add_trees(numbers, numbers))
    2
      4
        6
        8
      10
        12
          14
        16
    >>> print_tree(add_trees(tree(2), tree(3, [tree(4), tree(5)])))
    5
      4
      5
    >>> print_tree(add_trees(tree(2, [tree(3)]), tree(2, [tree(3), tree(4)])))
    4
      6
      4
    >>> print_tree(add_trees(tree(2, [tree(3, [tree(4), tree(5)])]), \
    tree(2, [tree(3, [tree(4)]), tree(5)])))
    4
      6
        8
        5
      5
    """
    "*** YOUR CODE HERE ***"
```
