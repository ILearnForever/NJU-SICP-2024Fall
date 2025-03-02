# Problem 3: Climb Stairs (200pts)

Nolan lives on the sixth floor of the dormitory building and feels frustrated about climbing such a long flight of stairs every day. He is wondering how many different ways he can go up the stairs. He knows that going up the stairs requires `n` steps, where `n` is a positive integer, and he can either take 1 or 2 steps each time.

Please help him write a function `count_stair_ways` which takes in the total steps `n` and returns the number of ways to climb up a flight of `n` stairs.

```python
def count_stair_ways(n):
    """Returns the number of ways to climb up a flight of
    n stairs, moving either 1 step or 2 steps at a time.
    >>> count_stair_ways(3)
    3
    >>> count_stair_ways(4)
    5
    >>> count_stair_ways(10)
    89
    """
    "*** YOUR CODE HERE ***"

```

Nolan realized that he could take more steps at a time! Now he is able to take up to and including `k` steps at a time, where `k` is a positive integer.

Write a function `count_k` that takes in the total steps `n` and maximum steps `k` at a time, then return the number of ways to climb up a flight of `n` stairs. (`k` may be larger than `n`)

> **Hint:** Your solution will follow a very similar logic to what you did in `count_stair_ways`.

```python
def count_k(n, k):
    """Counts the number of paths to climb up a flight of n stairs,
    taking up to and including k steps at a time.
    >>> count_k(3, 3) # 3, 2 + 1, 1 + 2, 1 + 1 + 1
    4
    >>> count_k(4, 4)
    8
    >>> count_k(10, 3)
    274
    >>> count_k(300, 1) # Only one step at a time
    1
    >>> count_k(3, 5) # Take no more than 3 steps
    4
    """
    "*** YOUR CODE HERE ***"
```
