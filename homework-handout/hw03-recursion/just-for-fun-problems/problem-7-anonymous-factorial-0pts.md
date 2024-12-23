# Problem 7: Anonymous factorial (0pts)

The recursive factorial function can be written as a single expression by using a [conditional expression](https://docs.python.org/py3k/reference/expressions.html#conditional-expressions).

```python
>>> fact = lambda n: 1 if n == 1 else mul(n, fact(sub(n, 1)))
>>> fact(5)
120
```

> The ternary operator `<a> if <bool-exp> else <b>` evaluates to `<a>` if `<bool-exp>` is truthy and evaluates to `<b>` if `<bool-exp>` is false-y.

However, this implementation relies on the fact (no pun intended) that `fact` has a name, to which we refer in the body of `fact`. To write a recursive function, we have always given it a name using a `def` or assignment statement so that we can refer to the function within its own body. In this question, your job is to define fact recursively without giving it a name!

Write an expression that computes `n` factorial using only call expressions, conditional expressions, and lambda expressions (no assignment or def statements). _Note in particular that you are not allowed to use `make_anonymous_factorial` in your return expression._ The `sub` and `mul` functions from the `operator` module are the only built-in functions required to solve this problem:

```python
from operator import sub, mul


def make_anonymous_factorial():
    """Return the value of an expression that computes factorial.

    >>> make_anonymous_factorial()(5)
    120
    >>> from construct_check import check
    >>> # ban any assignments or recursion
    >>> check(HW_SOURCE_FILE, 'make_anonymous_factorial', ['Assign', 'AugAssign', 'FunctionDef', 'Recursion'])
    True
    """
    return 'YOUR_EXPRESSION_HERE'
```
