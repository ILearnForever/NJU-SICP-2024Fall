# Problem 6: Multiadder (100pts)

An order `1` numeric function is a function that takes a number and returns a number. An order `2` numeric function is a function that takes a number and returns an order `1` numeric function. Likewise, an order `n` numeric function is a function that takes a number and returns an order `n-1` numeric function. The argument sequence of a nested call expression is the sequence of all arguments in all subexpressions, in the order they appear. For example, the expression `f(3)(4)(5)(6)(7)` has the argument sequence 3, 4, 5, 6, 7. Note that all numeric functions are pure functions.

Implement `multiadder`, which takes a positive integer `n` and returns an order `n` numeric function that sums an argument sequence of length `n`.

```python
def multiadder(n):
    """Return a function that takes N arguments, one at a time, and adds them.
    >>> f = multiadder(3)
    >>> f(5)(6)(7) # 5 + 6 + 7
    18
    >>> multiadder(1)(5)
    5
    >>> multiadder(2)(5)(6) # 5 + 6
    11
    >>> multiadder(4)(5)(6)(7)(8) # 5 + 6 + 7 + 8
    26
    >>> from construct_check import check
    >>> # Make sure multiadder is a pure function.
    >>> check(HW_SOURCE_FILE, 'multiadder',
    ...       ['Nonlocal', 'Global'])
    True
    """
    "*** YOUR CODE HERE ***"
```
