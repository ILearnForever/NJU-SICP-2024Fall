# Problem 3: Largest Factor (100pts)

Write a function that takes an integer $$x$$𝑥 that is **greater than** $$1$$1 and returns the largest integer that is smaller than $$x$$𝑥 and evenly divides $$x$$𝑥.

```python
def largest_factor(x):
    """Return the largest factor of x that is smaller than x.

    >>> largest_factor(15) # factors are 1, 3, 5
    5
    >>> largest_factor(80) # factors are 1, 2, 4, 5, 8, 10, 16, 20, 40
    40
    >>> largest_factor(13) # factor is 1 since 13 is prime
    1
    """
    "*** YOUR CODE HERE ***"
```

> Hint1: To check if b evenly divides a, you can use the expression a % b == 0, which can be read as, "the remainder of dividing a by b is 0."
>
> Hint2: You may want to review what is [iteration](http://www.composingprograms.com/pages/15-control.html#iteration)?
