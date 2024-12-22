# Question 3: Trees

> Submit your answers with `python ok -q q3 -u`.

**Note**: Read over the `Tree` class in `lab07.py`. Make sure you understand the doctests.

```python
>>> t = Tree(1, Tree(2))
______

>>> t = Tree(1, [Tree(2)])
>>> t.label
______

>>> t.branches[0]
______

>>> t.branches[0].label
______

>>> t.label = t.branches[0].label
>>> t
______

>>> t.branches.append(Tree(4, [Tree(8)]))
>>> len(t.branches)
______

>>> t.branches[0]
______

>>> t.branches[1]
______
```
