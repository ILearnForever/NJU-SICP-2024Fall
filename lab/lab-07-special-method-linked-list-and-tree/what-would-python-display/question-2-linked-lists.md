# Question 2: Linked Lists

> Submit your answers with `python ok -q q2 -u`.

**Note**: Read over the `Link` class in `lab07.py`. Make sure you understand the doctests.

```python
>>> link = Link(1000)
>>> link.first
______

>>> link.rest is Link.empty
______

>>> link = Link(1000, 2000)
______

>>> link = Link(1000, Link())
______
```

```python
>>> link = Link(1, Link(2, Link(3)))
>>> link.first
______

>>> link.rest.first
______

>>> link.rest.rest.rest is Link.empty
______

>>> link.first = 9001
>>> link.first
______

>>> link.rest = link.rest.rest
>>> link.rest.first
______

>>> link = Link(1)
>>> link.rest = link
>>> link.rest.rest.rest.rest.first
______

>>> link = Link(2, Link(3, Link(4)))
>>> link2 = Link(1, link)
>>> link2.first
______

>>> link2.rest.first
______
```

```python
>>> link = Link(5, Link(6, Link(7)))
>>> link                 # Look at the __repr__ method of Link
______

>>> print(link)          # Look at the __str__ method of Link
______
```
