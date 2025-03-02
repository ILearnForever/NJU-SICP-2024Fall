# Question 1: Control

> **In What Would Python Display problems, always follow these rules:**
>
> > For each of the expressions in the table below, write the output displayed by the interactive Python interpreter when the expression is valued. The output may have multiple lines. Each expression has at least one line of output.
> >
> > * If an error occurs, write `Error`, but include all output displayed before the error.
> > * If an expression would take forever to evaluate, write `Forever`.
> >
> > The interactive interpreter displays the value of a successfully evaluated expression, unless it is `None`.
>
> Check your answers with `python ok -q q1 -u`. **You need not modify any files to answer WWPD problems!!**

```python
>>> def xk(c, d):
...     if c == 4:
...         return 6
...     elif d >= 4:
...         return 6 + 7 + c
...     else:
...         return 25
>>> xk(10, 10)
______

>>> xk(10, 6)
______

>>> xk(4, 6)
______

>>> xk(0, 0)
______
```

```python
>>> def how_big(x):
...     if x > 10:
...         print('huge')
...     elif x > 5:
...         return 'big'
...     elif x > 0:
...         print('small')
...     else:
...         print("nothin'")
>>> how_big(7)
______

>>> how_big(12)
______

>>> how_big(1)
______

>>> how_big(-1)
______
```

```python
>>> n = 3
>>> while n >= 0:
...     n -= 1
...     print(n)
______
```

<details>

<summary>Hint</summary>

Make sure your `while` loop conditions eventually evaluate to a false value, or they'll never stop! Type `Ctrl-C` will stop infinite loops in the interpreter.

</details>

```python
>>> positive = 28
>>> while positive:
...     print("positive?")
...     positive -= 3
______
```

```python
>>> positive = -9
>>> negative = -12
>>> while negative:
...     if positive:
...         print(negative)
...     positive += 3
...     negative += 3
______
```
