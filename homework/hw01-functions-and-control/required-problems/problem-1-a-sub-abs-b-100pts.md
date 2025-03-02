# Problem 1: A Sub Abs B (100pts)

Fill in the blanks in the following function for subtracting $$a$$ with the absolute value of $$b$$, without calling `abs`. You may **not** modify any of the provided code other than the two blanks.

```python
from operator import add, sub, mul, neg

def a_sub_abs_b(a, b):
    """Return a-abs(b), but do not call abs.

    >>> a_sub_abs_b(2, 3)
    -1
    >>> a_sub_abs_b(2, -3)
    -1
    >>> # a check that you didn't change the return statement!
    >>> import inspect, re
    >>> re.findall(r'^\s*(return .*)', inspect.getsource(a_sub_abs_b), re.M)
    ['return h(a, b)']
    """
    if b >= 0:
        h = _____
    else:
        h = _____
    return h(a, b)
```

> Hint: You may want to use `add`, `sub`, `mul` and/or `neg` that imported from `operator`.
>
> Here is [the documentation of these operators](https://docs.python.org/3/library/operator.html#mapping-operators-to-functions).

> Test your implementation with `python ok -q a_sub_abs_b`.
>
> 在大多数作业中，大家可以用`python ok -q 函数名`的方式来测试对应的函数，后面就不再赘述了。
