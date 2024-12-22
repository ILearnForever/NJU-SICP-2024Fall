# Problem 2.2: Mutable Mapping (100pts)

Implement `deep_map_mut(func, link)`, which applies a function `func` onto all elements in the given linked list `link`. If an element is itself a non-empty linked list, apply `func` to each of its elements, and so on.

Your implementation should mutate the original linked list. **DO NOT create any new linked lists and and DO NOT return the modified Link object.**

> **Hint1**: The built-in `isinstance` function may be useful, but be careful about `Link.empty`.
>
> ```python
> >>> s = Link(1, Link(2, Link(3, Link(4))))
> >>> isinstance(s, Link)
> True
> >>> isinstance(s, int)
> False
> >>> isinstance(Link.empty, Link)
> False
> ```

> **Construct Check**: The last doctest of this question ensures that you do not create new linked lists. If you are failing this doctest, ensure that you are not creating link lists by calling the constructor, i.e.
>
> ```python
> s = Link(1)
> ```

```python
def deep_map_mut(func, link):
    """Mutates a deep link by replacing each item found with the
    result of calling func on the item. DO NOT create new Links (so
    no use of Link's constructor) and DO NOT return the modified Link object.

    >>> link1 = Link(3, Link(Link(4), Link(5, Link(6))))
    >>> # Disallow the use of making new Links before calling deep_map_mut
    >>> Link.__init__, hold = lambda *args: print("Do not steal chicken!"), Link.__init__
    >>> try:
    ...     deep_map_mut(lambda x: x * x, link1)
    ... finally:
    ...     Link.__init__ = hold
    >>> print(link1)
    <9 <16> 25 36>
    """
    "*** YOUR CODE HERE ***"
```
