# Problem 6: Double Factorial (100pts)

Let's write a function `double_factorial`, which takes a positive integer $$n$$ and returns its double factorial.

Double factorial of a positive integer $$n$$, denoted by $$n!!$$, is defined as

$$
n!!=\prod_{i=0}^{\lceil\frac{n}{2}\rceil-1}(n-2i)=n\times(n-2)\times(n-4)\times\dots
$$

> This problem is an advanced version of Problem 2, Lab 01.

```python
def double_factorial(n, k):
    """Compute the double factorial of n.

    >>> double_factorial(6)  # 6 * 4 * 2
    48
    >>> double_factorial(5)  # 5 * 3 * 1
    15
    >>> double_factorial(3)  # 3 * 1
    3
    >>> double_factorial(1)  # 1
    1
    """
    "*** YOUR CODE HERE ***"
```
