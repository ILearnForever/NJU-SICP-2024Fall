# Problem 2: Ping-pong (200pts)

The ping-pong sequence counts up starting from 1 and is always either counting up or counting down. At element `k`, the direction switches if `k` is a multiple of 6 or contains the digit 6. The first 30 elements of the ping-pong sequence are listed below, with direction swaps marked using brackets at the 6th, 12th, 16th, 18st, 24th, 26th and 30th elements:

| **Index**         | **1**  | **2**     | **3**  | **4**     | **5**  | **\[6]**  | **7**  | **8**     | **9**  | **10**    |
| ----------------- | ------ | --------- | ------ | --------- | ------ | --------- | ------ | --------- | ------ | --------- |
| PingPong Value    | 1      | 2         | 3      | 4         | 5      | \[6]      | 5      | 4         | 3      | 2         |
| **Index (cont.)** | **11** | **\[12]** | **13** | **14**    | **15** | **\[16]** | **17** | **\[18]** | **19** | **20**    |
| PingPong Value    | 1      | \[0]      | 1      | 2         | 3      | \[4]      | 3      | \[2]      | 3      | 4         |
| **Index (cont.)** | **21** | **22**    | **23** | **\[24]** | **25** | **\[26]** | **27** | **28**    | **29** | **\[30]** |
| PingPong Value    | 5      | 6         | 7      | \[8]      | 7      | \[6]      | 7      | 8         | 9      | \[10]     |

Implement a function `pingpong` that returns the nth element of the ping-pong sequence _without using any assignment statements_.

_Use recursion - the tests will fail if you use any assignment statements._

> _Hint1_: If you're stuck, first try implementing `pingpong` using assignment statements and a `while` statement. Then, to convert this into a recursive solution, write a helper function that has a parameter for each variable that changes values in the body of the while loop.
>
> _Hint2_: You may need a helper function `contains_six` to check whether the given number contains digit 6.

> 注意：我们期望你的“递归”代码**和等价的“循环”代码有差不多的效率**。这道题的`n`可能很大，你应该试试你的代码计算`pingpong(500)`要花多少时间（一瞬间？几秒钟？还是几千年？）才能得到结果。

```python
def pingpong(n):
    """Return the nth element of the ping-pong sequence.

    >>> pingpong(7)
    5
    >>> pingpong(8)
    4
    >>> pingpong(15)
    3
    >>> pingpong(21)
    5
    >>> pingpong(22)
    6
    >>> pingpong(30)
    10
    >>> pingpong(68)
    0
    >>> pingpong(69)
    1
    >>> pingpong(70)
    0
    >>> pingpong(71)
    -1
    >>> pingpong(72)
    -2
    >>> pingpong(100)
    6
    >>> from construct_check import check
    >>> # ban assignment statements
    >>> check(HW_SOURCE_FILE, 'pingpong', ['Assign', 'AugAssign'])
    True
    """
    "*** YOUR CODE HERE ***"
```
