# Question 1: Repr-esentation

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

**Note**: This is not the typical way `repr` is used, nor is this way of writing `repr` recommended. This problem is mainly just to make sure you understand how `repr` and `str` work.

```python
class A:
    def __init__(self, x):
        self.x = x

    def __repr__(self):
         return self.x

    def __str__(self):
         return self.x * 2

class B:
    def __init__(self):
         print('boo!')
         self.a = []

    def add_a(self, a):
         self.a.append(a)

    def __repr__(self):
         print(len(self.a))
         ret = ''
         for a in self.a:
             ret += str(a)
         return ret
```

```python
>>> A('one')
______

>>> print(A('one'))
______

>>> repr(A('two'))
______

>>> b = B()
______

>>> b.add_a(A('a'))
>>> b.add_a(A('b'))
>>> b
______
```
