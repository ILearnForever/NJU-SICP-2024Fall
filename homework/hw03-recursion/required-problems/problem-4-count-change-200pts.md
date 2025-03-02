# Problem 4: Count change (200pts)

Denomination is a proper description of a currency amount, usually for coins or banknotes. For example, we have 1 Yuan coins and 100 Yuan bills in Chinese Yuan.

A currency system can be described by a special function that takes in an argument `ith` and returns the ith smallest denomination in that currency system. For example, the following money function describes Chinese Yuan (1 Yuan, 5 Yuan, 10 Yuan, 20 Yuan, 50 Yuan and 100 Yuan). `chinese_yuan(2)` returns `5` as 5 Yuan is the second smallest denomination.

When `ith` does not correspond to any denomination, money function returns `None`. For example, `chinese_yuan(7)` yields `None` since there are only 6 distinct denominations in Chinese Yuan.

```python
def chinese_yuan(ith):
    if ith == 1:
        return 1
    if ith == 2:
        return 5
    if ith == 3:
        return 10
    if ith == 4:
        return 20
    if ith == 5:
        return 50
    if ith == 6:
        return 100
```

Given an amount of money `total` and a currency system, a set of banknotes (coins) makes change for `total` if sum of their values is exactly `total`. For example, the following sets make change for 15 Chinese Yuan:

* 15\*1-Yuan
* 10\*1-Yuan + 1\*5-Yuan
* 5\*1-Yuan + 2\*5-Yuan
* 5\*1-Yuan + 1\*10-Yuan
* 3\*5-Yuan
* 1\*5-Yuan + 1\*10-Yuan

Thus, there are 6 different ways to make change for 15 Chinese Yuan.

Write a recursive function `count_change` that takes a positive integer `total` and a money function `money` and returns the number of ways to make change for `total` under the currency system described by `money`.

> _Hint_: Refer to the [implementation](http://www.composingprograms.com/pages/17-recursive-functions.html#example-partitions) of `count_partitions` for an example of how to count the ways to sum up to a total with smaller parts. If you need to keep track of more than one value across recursive calls, consider writing a helper function and pass around the intermediate values as the arguments of the helper function.

```python
def count_change(total, money):
    """Return the number of ways to make change for total,
    under the currency system described by money.

    >>> def chinese_yuan(ith):
    ...     if ith == 1:
    ...         return 1
    ...     if ith == 2:
    ...         return 5
    ...     if ith == 3:
    ...         return 10
    ...     if ith == 4:
    ...         return 20
    ...     if ith == 5:
    ...         return 50
    ...     if ith == 6:
    ...         return 100
    >>> def us_cent(ith):
    ...     if ith == 1:
    ...         return 1
    ...     if ith == 2:
    ...         return 5
    ...     if ith == 3:
    ...         return 10
    ...     if ith == 4:
    ...         return 25
    >>> count_change(15, chinese_yuan)
    6
    >>> count_change(49, chinese_yuan)
    44
    >>> count_change(49, us_cent)
    39
    >>> count_change(49, lambda x: 2 ** (x - 1))
    692
    >>> from construct_check import check
    >>> # ban iteration
    >>> check(HW_SOURCE_FILE, 'count_change', ['While', 'For'])
    True
    """
    "*** YOUR CODE HERE ***"
```
