# Problem 3.1: Cumulative Mul (100pts)

Write a function `cumulative_mul` that mutates the Tree `t` so that each node's label becomes the product of all labels in the subtree rooted at the node.

```python
def cumulative_mul(t):
    """Mutates t so that each node's label becomes the product of all labels in
    the corresponding subtree rooted at t.

    >>> t = Tree(1, [Tree(3, [Tree(5)]), Tree(7)])
    >>> cumulative_mul(t)
    >>> t
    Tree(105, [Tree(15, [Tree(5)]), Tree(7)])
    """
    "*** YOUR CODE HERE ***"
```

> **Hint1**: The answer is simple and neat. If your answer is too complicated, you might want to review [Section 2.3](https://sicp.pascal-lab.net/2024/labs/lab07/2_3.html) and compare the difference between the oop-style `Tree` and the functional-style `tree`.
>
> **Hint2**: The label of a tree might not be an integer since operator `*` can be overloaded just as you've done before.
