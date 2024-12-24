# Problem 4: If Function vs Statement (100pts)

```python
def if_function(condition, true_result, false_result):
    """Return true_result if condition is a true value, and
    false_result otherwise.

    >>> if_function(True, 2, 3)
    2
    >>> if_function(False, 2, 3)
    3
    >>> if_function(3==2, 3+2, 3-2)
    1
    >>> if_function(3>2, 3+2, 3-2)
    5
    """
    if condition:
        return true_result
    else:
        return false_result
```

Despite the doctests above, this function actually does not do the same thing as an `if` statement in all cases.

To prove this fact, write functions `c`, `t`, and `f` such that `with_if_statement` prints the number 2, but `with_if_function` prints both 1 and 2.

```python
def with_if_statement():
    """
    >>> result = with_if_statement()
    2
    >>> print(result)
    None
    """
    if c():
        return t()
    else:
        return f()

def with_if_function():
    """
    >>> result = with_if_function()
    1
    2
    >>> print(result)
    None
    """
    return if_function(c(), t(), f())

def c():
    "*** YOUR CODE HERE ***"

def t():
    "*** YOUR CODE HERE ***"

def f():
    "*** YOUR CODE HERE ***"
```

> Hint: If you are having a hard time identifying how an if statement and if\_function differ, consider [the rules of evaluation for if statements](http://www.composingprograms.com/pages/15-control.html#conditional-statements) and [call expressions](http://www.composingprograms.com/pages/12-elements-of-programming.html#call-expressions).

> For this problem, you can test your implementation with:
>
> * `python ok -q with_if_statement`
> * `python ok -q with_if_function`
