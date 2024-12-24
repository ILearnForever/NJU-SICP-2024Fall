# Problem 1: Lambdas and Currying (100pts)

We can transform multiple-argument functions into a chain of single-argument, higher order functions by taking advantage of lambda expressions. This is useful when dealing with functions that take only single-argument functions. We will see some examples of these later on.

Write a function `lambda_curry2` that will curry any two argument function using lambdas. See the doctest or refer to Section 1.6.6 in the [textbook](http://www.composingprograms.com/pages/16-higher-order-functions.html) if you're not sure what this means.

**Your solution to this problem should fit entirely on the return line.** You can try writing it first without this restriction, but rewrite it after in one line to test your understanding of this topic.

> To test your implementation, run `python ok -q lambda_curry2`.

```python
def lambda_curry2(func):
    """
    Returns a Curried version of a two-argument function FUNC.
    >>> from operator import add, mul, mod
    >>> curried_add = lambda_curry2(add)
    >>> add_three = curried_add(3)
    >>> add_three(5)
    8
    >>> curried_mul = lambda_curry2(mul)
    >>> mul_5 = curried_mul(5)
    >>> mul_5(42)
    210
    >>> lambda_curry2(mod)(123)(10)
    3
    >>> # You aren't expected to understand the code of this test.
    >>> # It's just here to check that definition of lambda_curry2 is just a return statement.
    >>> import inspect, ast
    >>> [type(x).__name__ for x in ast.parse(inspect.getsource(lambda_curry2)).body[0].body]
    ['Expr', 'Return']
    """
    return ______
```
