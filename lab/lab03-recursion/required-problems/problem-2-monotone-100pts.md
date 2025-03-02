# Problem 2: Monotone (100pts)

A number is said to have _monotone_ digits if its digits have an non-decreasing order from left to right when written down. For example, `1234` and `24555` have monotone digits, while `22000130` and `2024` don't.

Now, please write a recursive function `is_monotone`, which takes as input a number `n` and returns whether `n` has monotone digits. Specifically, `is_monotone` returns `True` if `n` has monotone digits, and returns `False` if not.

```python
def is_monotone(n):
    """Returns whether n has monotone digits.
    Implement using recursion!

    >>> is_monotone(22000130)
    False
    >>> is_monotone(1234)
    True
    >>> is_monotone(24555)
    True
    >>> # Do not use while/for loops!
    >>> from construct_check import check
    >>> # ban iteration
    >>> check(LAB_SOURCE_FILE, 'is_monotone', ['While', 'For'])
    True
    """
    "*** YOUR CODE HERE ***"
```
