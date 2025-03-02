# Problem 5: Hailstone (100pts)

Write a generator that outputs the hailstone sequence from hw01.

Here's a quick reminder of how the hailstone sequence is defined:

1. Pick a positive integer $$n$$ as the start.
2. If $$n$$ is even, divide it by 2.
3. If $$n$$ is odd, multiply it by 3 and add 1.
4. Continue this process until $$n$$ is 1.

For some extra practice, try writing a solution using recursion. Since hailstone returns a generator, you can `yield from` a call to hailstone!

```python
def hailstone(n):
    """Return a generator that outputs the hailstone sequence.

    >>> for num in hailstone(10):
    ...     print(num)
    10
    5
    16
    8
    4
    2
    1
    """
    "*** YOUR CODE HERE ***"
```
