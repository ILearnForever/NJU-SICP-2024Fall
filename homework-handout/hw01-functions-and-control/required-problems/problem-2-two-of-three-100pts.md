# Problem 2: Two of Three (100pts)

Write a function that takes three positive numbers and returns the sum of the squares of the two largest numbers. **Use only a single line for the body of the function.**

```python
def two_of_three(x, y, z):
    """Return a*a + b*b, where a and b are the two largest members of the
    positive numbers x, y, and z.

    >>> two_of_three(1, 2, 3)
    13
    >>> two_of_three(5, 3, 1)
    34
    >>> two_of_three(10, 2, 8)
    164
    >>> two_of_three(5, 5, 5)
    50
    >>> # check that your code consists of nothing but an expression (this docstring)
    >>> # and a return statement
    >>> import inspect, ast
    >>> [type(x).__name__ for x in ast.parse(inspect.getsource(two_of_three)).body[0].body]
    ['Expr', 'Return']
    """
    return _____
```

> Hint: Consider using the max or min function:
>
> ```
> >>> max(1, 2, 3)
> 3
> >>> min(-1, -2, -3)
> -3
> ```
