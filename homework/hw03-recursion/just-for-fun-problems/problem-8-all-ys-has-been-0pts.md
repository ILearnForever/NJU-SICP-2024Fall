# Problem 8: All-Ys Has Been (0pts)

Given mystery function `Y`, complete `fib_maker` and `number_of_six_maker` so that the given doctests work correctly.

When `Y` is called on `fib_maker`, it should return a function which takes a positive integer `n` and returns the `n`th Fibonacci number.

Similarly, when `Y` is called on `number_of_six_maker` it should return a function that takes a positive integer `x` and returns the number of times the digit 6 appears in `x`.

> Hint: You may use the ternary operator `<a> if <bool-exp> else <b>`, which evaluates to `<a>` if `<bool-exp>` is truthy and evaluates to `<b>` if `<bool-exp>` is false-y.

```python
def Y(f): return (lambda x: x(x))(lambda x: f(lambda z: x(x)(z)))
def fib_maker(f): return lambda r: 'YOUR_EXPRESSION_HERE'
def number_of_six_maker(f): return lambda r: 'YOUR_EXPRESSION_HERE'


my_fib = Y(fib_maker)
my_number_of_six = Y(number_of_six_maker)

# This code sets up doctests for my_fib and my_number_of_six.

my_fib.__name__ = 'my_fib'
my_fib.__doc__ = """Given n, returns the nth Fibonacci nuimber.

>>> my_fib(0)
0
>>> my_fib(1)
1
>>> my_fib(2)
1
>>> my_fib(3)
2
>>> my_fib(4)
3
>>> my_fib(5)
5
"""

my_number_of_six.__name__ = 'my_number_of_six'
my_number_of_six.__doc__ = """Return the number of 6 in each digit of a positive integer n.

>>> my_number_of_six(666)
3
>>> my_number_of_six(123456)
1
"""
```

Remember to use Ok to test your code:

```shell
$ python ok -q my_fib
$ python ok -q my_number_of_six
```
