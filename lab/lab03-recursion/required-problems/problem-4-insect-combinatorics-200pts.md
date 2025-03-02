# Problem 4: Insect Combinatorics (200pts)

Consider an insect in an `M` by `N` grid. The insect starts at the bottom left corner, `(0, 0)`, and wants to end up at the top right corner, `(M-1, N-1)`. The insect is only capable of moving right or up by one step (e.g., from `(0, 0)` to `(0, 1)` or `(1, 0)`).

Write a function `paths` that takes a grid's length `M` and width `N` as input, then `paths` is supposed to return the number of different paths the insect can take from the start to the goal. (There is a [closed-form](https://zhidao.baidu.com/question/215075856.html) solution to this problem, but try to answer it procedurally using recursion.)

![grid](https://sicp.pascal-lab.net/2024/labs/lab03/images/grid.jpg)

For example, a 2 by 2 grid has a total of two ways for the insect to move from the start to the goal. For a 3 by 3 grid, the insect has 6 different paths (only 3 are shown above).

```python
def paths(m, n):
    """Return the number of paths from one corner of an
    M by N grid to the opposite corner.

    >>> paths(2, 2)
    2
    >>> paths(5, 7)
    210
    >>> paths(117, 1)
    1
    >>> paths(1, 157)
    1
    """
    "*** YOUR CODE HERE ***"
```
