# Problem 4: Fold Tree (0pts)

> Use `python ok -q tree` to test your implementation.

It is often the case that we want to fold a tree into a value. Consider the following implementations of `count_leaves` and `label_sum`.

```python
def count_leaves(t):
    """Count the leaves of a tree."""
    if is_leaf(t):
        return 1
    result = 0
    for b in branches(t):
        result += count_leaves(b)
    return result

def label_sum(t):
    """Sum up the labels of all nodes in a tree."""
    if is_leaf(t):
        return label(t)
    result = label(t)
    for b in branches(t):
        result += label_sum(b)
    return result
```

or, by clever usage of function `sum` and list comprehension, we can equivalently write

```python
def count_leaves(t):
    """Count the leaves of a tree."""
    if is_leaf(t):
        return 1
    return sum([count_leaves(b) for b in branches(t)])

def label_sum(t):
    """Sum up the labels of all nodes in a tree."""
    if is_leaf(t):
        return label(t)
    return label(t) + sum([label_sum(b) for b in branches(t)])
```

You may find these implementations look quite similar, as they both:

1. return something immediately at a base case when `t` is a leaf
2. recursively apply the function to branches, and sum up the results of the branches

To capture this insight, we can define a function `fold_tree` which takes in a function `base_func` and a function `merge_func`. You can feel free to define the meaning and usage of `base_func` and `merge_func`. Then use `fold_tree` to implement `count_leaves`, `label_sum` and `preorder`.

```python
def fold_tree(t, base_func, merge_func):
    """Fold tree into a value according to base_func and merge_func"""
    "*** YOUR CODE HERE ***"

```

```python
def count_leaves(t):
    """Count the leaves of a tree.

    >>> t = tree(1, [tree(2), tree(3, [tree(4), tree(5)])])
    >>> count_leaves(t)
    3
    """
    return fold_tree(t, 'YOUR EXPRESSION HERE', 'YOUR EXPRESSION HERE')


def label_sum(t):
    """Sum up the labels of all nodes in a tree.

    >>> t = tree(1, [tree(2), tree(3, [tree(4), tree(5)])])
    >>> label_sum(t)
    15
    """
    return fold_tree(t, 'YOUR EXPRESSION HERE', 'YOUR EXPRESSION HERE')


def preorder(t):
    """Return a list of the entries in this tree in the order that they
    would be visited by a preorder traversal.

    >>> t = tree(1, [tree(2), tree(3, [tree(4), tree(5)])])
    >>> preorder(t)
    [1, 2, 3, 4, 5]
    """
    return fold_tree(t, 'YOUR EXPRESSION HERE', 'YOUR EXPRESSION HERE')

```

Since functions are values in Python, we can also use `fold_tree` to fold a tree to a function. We can simply use `fold_tree` and curring to define a function `has_int` which checks if a given integer is contained in a tree:

```python
def has_int(tree, i): # Without fold_tree
    """Return if an integer is contained in a tree

    >>> has_int(tree(1, [tree(2, tree(3)), tree(4)]), 1)
    True
    >>> has_int(tree(1, [tree(2, tree(3)), tree(4)]), 5)
    False
    """
    return label(tree) == i or any([has_int(b) for b in branches(tree)])

def has_int(tree, i): # With fold_tree
    """Return if an integer is contained in a tree

    >>> has_int(tree(1, [tree(2, [tree(3)]), tree(4)]), 1)
    True
    >>> has_int(tree(1, [tree(2, [tree(3)]), tree(4)]), 5)
    False
    """

    def base_func(l):
        return lambda i: l == i
    def merge_func(l, bs):
        return lambda i: l == i or any([b(i) for b in bs])

    return fold_tree(tree, base_func, merge_func)(i)
```

> Note: If you don't know `any`, try "help(any)" in python interactive shell or searches the documentation.

Now, use the same technique to define `has_path`:

```python
def has_path_fold(t, word):
    """Return whether there is a path in a tree where the entries along the path
    spell out a particular word.

    >>> greetings = tree('h', [tree('i'),
    ...                        tree('e', [tree('l', [tree('l', [tree('o')])]),
    ...                                   tree('y')])])
    >>> print_tree(greetings)
    h
      i
      e
        l
          l
            o
        y
    >>> has_path_fold(greetings, 'h')
    True
    >>> has_path_fold(greetings, 'i')
    False
    >>> has_path_fold(greetings, 'hi')
    True
    >>> has_path_fold(greetings, 'hello')
    True
    >>> has_path_fold(greetings, 'hey')
    True
    >>> has_path_fold(greetings, 'bye')
    False
    """
    assert len(word) > 0, 'no path for empty word.'
    return fold_tree(t, 'YOUR EXPRESSION HERE', 'YOUR EXPRESSION HERE')
```
