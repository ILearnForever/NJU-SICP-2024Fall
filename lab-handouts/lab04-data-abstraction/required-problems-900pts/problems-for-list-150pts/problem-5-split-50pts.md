# Problem 5: Split (50pts)

`my_split` takes in a list `l` and a function `f` and splits the list `l` into two separate (i.e., a pair of) lists, so that for any element `e` in the first returned list, `f(e)` evaluates to `True`; and for any element `e` in the second returned list, `f(e)` evaluates to `False`.

It is guaranteed that

1. `f` is a pure function
2. `f` always terminates and
3. `f` returns either `True` or `False`

Such functions are called _predicat&#x65;_&#x73;, a term from the field of logic.

> _Hint_: use list comprehensions.

```python
def my_split(f, l):
    """Splits the list into a pair of lists according to predicate f.
    >>> my_split(lambda x: True, [1, 2, 3, 4]) # All elements from l conforms to the predicate
    ([1, 2, 3, 4], [])
    >>> my_split(lambda x: x % 2 == 0, [1, 2, 3, 4]) # Split into even and odd numbers
    ([2, 4], [1, 3])
    >>> my_split(lambda x: x < 5, [3, 1, 4, 1, 5, 9, 2])
    ([3, 1, 4, 1, 2], [5, 9])
    >>> my_split(lambda x: not x, [True, False, True, True]) # There might be things other than integers
    ([False], [True, True, True])
    >>> is_ldx = lambda x: not x.startswith('24')
    >>> studentIDs = ['24122', '22122', '502024', '24183']
    >>> ldx, xdx = my_split(is_ldx, studentIDs)
    >>> ldx
    ['22122', '502024']
    >>> studentIDs # You should not mutate the original list
    ['24122', '22122', '502024', '24183']
    """
    "*** YOUR CODE HERE ***"
```
