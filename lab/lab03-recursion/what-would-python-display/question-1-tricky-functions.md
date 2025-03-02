# Question 1: Tricky Functions

> Submit your answers with `python ok -q q1 -u`.
>
> **In What Would Python Display problems, always follow these rules:**
>
> > For each of the expressions in the table below, write the output displayed by the interactive Python interpreter when the expression is valued. The output may have multiple lines or no lines.
> >
> > * If an error occurs, write `Error`, but include all output displayed before the error.
> > * If an expression evaluates to a function value, write `Function`.
> > * If an expression would take forever to evaluate, write `Forever`.
> > * If the interpretor prints nothing, write `Nothing`.

> **Secret:** The following questions are inspired by the problems some of you met in lab02/hw02.

```python
>>> def f(x):
...     return x * x
>>> g = lambda x: f(x + 1)
>>> g
______

>>> g(1)
______

>>> print(g(2))
______

>>> f = lambda x: f(x + 1)
>>> f(1)    # When is the return expression of a lambda expression executed?
______
```

```python
>>> def f1(n):
...     def f2(x):
...         if x == 0:
...             return 'cake'
...         else:
...             print('The cake is a lie.')
...             n -= x
...             return f2(n)
...     return f2
>>> f1(2)
______

>>> f1(2)(2)
______
```
