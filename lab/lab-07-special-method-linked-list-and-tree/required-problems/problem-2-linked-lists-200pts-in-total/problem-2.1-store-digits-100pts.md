# Problem 2.1: Store Digits (100pts)

Write a function `store_digits` that takes in an integer `n` and returns a linked list where each element of the list is a digit of `n`. Your solution should run in Linear time in the length of its input.

**Note**: You may not use `str`, `repr` or `reversed` in your implementation.

```python
def store_digits(n):
    """Stores the digits of a positive number n in a linked list.

    >>> s = store_digits(0)
    >>> s
    Link(0)
    >>> store_digits(2345)
    Link(2, Link(3, Link(4, Link(5))))
    >>> store_digits(8760)
    Link(8, Link(7, Link(6, Link(0))))
    >>> # a check for restricted functions
    >>> import inspect, re
    >>> cleaned = re.sub(r"#.*\\n", '', re.sub(r'"{3}[\s\S]*?"{3}', '', inspect.getsource(store_digits)))
    >>> print("Do not steal chicken!") if any([r in cleaned for r in ["str", "repr", "reversed"]]) else None
    """
    "*** YOUR CODE HERE ***"
```
