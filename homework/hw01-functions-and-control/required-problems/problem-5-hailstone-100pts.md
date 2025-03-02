# Problem 5: Hailstone (100pts)

Douglas Hofstadter's Pulitzer-prize-winning book, _Gödel, Escher, Bach_, poses the following mathematical puzzle.

1. Pick a positive integer $$x$$𝑥 as the start.
2. If $$x$$𝑥 is even, divide it by 2.
3. If $$x$$𝑥 is odd, multiply it by 3 and add 1.
4. Continue this process until $$x$$𝑥 is 1.

The number $$x$$𝑥 will travel up and down but eventually end at 1 (at least for all numbers that have ever been tried -- nobody has ever proved that the sequence will terminate). Analogously, a hailstone travels up and down in the atmosphere before eventually landing on earth.

> **Breaking News** (or at least the closest thing to that in math). There has been a recent development in the hailstone conjecture that shows that almost all numbers will eventually get to 1 if you repeat this process. This isn't a complete proof but a major breakthrough.

This sequence of values of $$x$$𝑥 is often called a Hailstone sequence. Write a function that takes a single argument with formal parameter name $$x$$𝑥, prints out the hailstone sequence starting at $$x$$𝑥, and returns the number of steps in the sequence:

```python
def hailstone(x):
    """Print the hailstone sequence starting at x and return its
    length.

    >>> a = hailstone(10)
    10
    5
    16
    8
    4
    2
    1
    >>> a
    7
    """
    "*** YOUR CODE HERE ***"
```

Hailstone sequences can get quite long! Try 27. What's the longest you can find?
