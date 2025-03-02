# Iterable Uses

We know that lists are one type of built-in iterable objects. You may have also encountered the `range(start, end)` function, which creates an iterable of ascending integers from start (inclusive) to end (exclusive).

```python
>>> for x in range(1, 6):
...     print(x)
...
1
2
3
4
5
```

Ranges are useful for many things, including performing some operations for a particular number of iterations or iterating through the indices of a list.

There are also some built-in functions that take in iterables and return useful results:

* `map(f, iterable)` - Creates iterator over `f(x)` for each `x` in `iterable`
* `filter(f, iterable)` - Creates iterator over `x` for each `x` in `iterable` if `f(x)`
* `zip(iter0, iter2)` - Creates iterator over co-indexed pairs `(x, y)` from both input iterables
* `reversed(iterable)` - Creates iterator over all the elements in the input iterable in reverse order
* `list(iterable)` - Creates a list containing all the elements in the input iterable
* `tuple(iterable)` - Creates a tuple containing all the elements in the input iterable
* `sorted(iterable)` - Creates a sorted list containing all the elements in the input iterable
* `enumerate(iterable)` - Creates iterator over pairs containing an index and the element corresponding to that index
