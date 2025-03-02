# Question 2: Squared Virahanka Fibonacci

> Submit your answers with `python ok -q q2 -u`.

> **Background:**
>
> In the Squared Virahanka Fibonacci sequence, each number in the sequence is the square of the sum of the previous two numbers in the sequence. The first 0th and 1st number in the sequence are 0 and 1, respectively. The recursive virfib\_sq function takes in an argument n and returns the nth number in the Square Virahanka Fibonacci sequence.

```python
>>> def virfib_sq(n):
...     print(n)
...     if n <= 1:
...         return n
...     return (virfib_sq(n - 1) + virfib_sq(n - 2)) ** 2

>>> virfib_sq
______

>>> r0 = virfib_sq(0)
______

>>> virfib_sq(1)
______

>>> r1 = virfib_sq(1)
______

>>> r2 = virfib_sq(2)
______

>>> r3 = virfib_sq(3)
______

>>> r3
______

>>> (r1 + r2) ** 2
______

>>> r4 = virfib_sq(4)
______

>>> r4
______
```
