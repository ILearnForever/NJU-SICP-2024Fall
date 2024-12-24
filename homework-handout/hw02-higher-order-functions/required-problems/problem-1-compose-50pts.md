# Problem 1: Compose (50pts)

Define a function `compose` so that `compose(h, g)(x)` returns `h(g(x))`. That is, `compose(h, g)` returns another function a function f, such that `f(x) = h(g(x))`.

```python
def compose(h, g):
    """Return a function f, such that f(x) = h(g(x)).
    
    >>> compose(square, triple)(5)
    225
    >>> double_inc = compose(increment, increment)
    >>> double_inc(3)
    5
    >>> double_inc(4)
    6
    """
    "*** YOUR CODE HERE ***"
```
