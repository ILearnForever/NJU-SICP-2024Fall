# List Comprehensiona

List comprehension is a compact and powerful way of creating new lists out of sequences. The general syntax for a list comprehension is the following:

```
[<expression> for <element> in <sequence> if <conditional>]
```

The syntax is designed to read like English: _"Compute the expression for each element in the sequence if the conditional is true for that element."_

Let's see an example:

```python
>>> [i**2 for i in [1, 2, 3, 4] if i % 2 == 0]
[4, 16]
```

Here, for each element `i` in `[1, 2, 3, 4]` that satisfies the condition `i % 2 == 0`, we evaluate the expression `i**2` and insert the resulting values into a new list. In other words, this list comprehension will create a new list that contains the square of each of the even elements of the original list.

If we were to write the example above using for and if statements, it would take more lines:

```python
>>> lst = []
>>> for i in [1, 2, 3, 4]:
...     if i % 2 == 0:
...         lst = lst + [i**2]
>>> lst
[4, 16]
```

> Note: The if clause in a list comprehension is optional. For example, we can just write:
>
> ```python
> >>> [i**2 for i in [1, 2, 3, 4]]
> [1, 4, 9, 16]
> ```
