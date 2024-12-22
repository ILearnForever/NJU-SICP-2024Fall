# Question 2

> Use Ok to test your knowledge with the following "What Would Python Display?" questions:
>
> ```shell
> python ok -q q2 -u
> ```
>
> **Important**: Type `Function` if you believe the answer is `<function...>`, `Error` if it errors, and `Nothing` if nothing is displayed.

```python
>>> class A:
...   x, y = 0, 0
...   def __init__(self):
...         return
>>> class B(A):
...   def __init__(self):
...         return
>>> class C(A):
...   def __init__(self):
...         return
>>> print(A.x, B.x, C.x)
______

>>> B.x = 2
>>> print(A.x, B.x, C.x)
______

>>> A.x += 1
>>> print(A.x, B.x, C.x)
______

>>> obj = C()
>>> obj.y = 1
>>> C.y == obj.y
______

>>> A.y = obj.y
>>> print(A.y, B.y, C.y, obj.y)
______
```
