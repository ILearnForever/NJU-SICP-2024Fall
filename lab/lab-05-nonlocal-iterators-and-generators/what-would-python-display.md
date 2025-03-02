# What Would Python Display?

> Use Ok to test your knowledge with the following "What Would Python Display?" questions:
>
> ```shell
> python ok -q wwpd -u
> ```
>
> **Important**: Enter `StopIteration` if a `StopIteration` exception occurs, `Error` if you believe a different error occurs, and `Iterator` if the output is an iterator object.

```python
>>> s = [1, 2, 3, 4]
>>> t = iter(s)
>>> next(s)
______

>>> next(t)
______

>>> next(t)
______

>>> iter(s)
______

>>> next(iter(s))
______

>>> next(iter(t))
______

>>> next(iter(s))
______

>>> next(iter(t))
______

>>> next(t)
______
```

```python
>>> r = range(6)
>>> r_iter = iter(r)
>>> next(r_iter)
______

>>> [x + 1 for x in r]
______

>>> [x + 1 for x in r_iter]
______

>>> next(r_iter)
______

>>> list(range(-2, 4))   # Converts an iterable into a list
______
```

```python
>>> map_iter = map(lambda x : x + 10, range(5))
>>> next(map_iter)
______

>>> next(map_iter)
______

>>> list(map_iter)
______

>>> for e in filter(lambda x : x % 2 == 0, range(1000, 1008)):
...     print(e)
______

>>> [x + y for x, y in zip([1, 2, 3], [4, 5, 6])]
______

>>> for e in zip([10, 9, 8], range(3)):
...   print(tuple(map(lambda x: x + 2, e)))
______
```
