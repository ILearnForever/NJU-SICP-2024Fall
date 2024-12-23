# Mutability

We say that an object is _mutable_ if its state can be changed as code executes, otherwise we call it _immutable_. The process of changing an object's state is called _mutation_. Examples of mutable objects include lists and dictionaries. Examples of objects that are not mutable include tuples and functions.

> Note: Remember to distinguish object mutation from variable assignment

```python
>>> l = [1, 2]
>>> l[0] = 114 # Lists are mutable
>>> l
[114, 2]
>>> t = (1, 2)
>>> t[0] = 114 # Tuples are immutable
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: 'tuple' object does not support item assignment
>>> t = (114, 2) # Variables can be reassigned, though
>>> t[0]
114
```

We have seen how to use the `==` operator to check if two expressions evaluate to the same **values**. We now introduce a new comparison operator, `is`, that checks if two expressions evaluate to the same **identities**.

Each object has its own identity. That means you can construct two objects that may look exactly the same but have different identities.

```python
>>> num1 = 257
>>> num2 = 257
>>> num1 == num2
True
>>> num1 is num2
False
>>> lst1 = [1, 2, 3, 4]
>>> lst2 = [1, 2, 3, 4]
>>> lst1 == lst2
True
>>> lst1 is lst2
False
```

> You may find that the behavior of `is` in some cases is different from what we suggest. For example,
>
> ```python
> >>> num1 = 10
> >>> num2 = 10
> >>> num1 is num2
> True
> ```
>
> This is because python will cache some 'small' objects (i.e., small numbers, short strings, booleans, `None`, ...). To check more counter examples, see this [page](https://stackoverflow.com/questions/15171695/whats-with-the-integer-cache-maintained-by-the-interpreter)
>
> Also note that python will never cache _mutable_ objects.

Here, although the lists referred by lst1 and lst2 have exactly the same contents, they are not the same object. In other words, they are the same in terms of equality, but not in terms of identity (think about twins that look exactly the same but are in fact two different persons).

This is important in the discussion of mutability because when we mutate an object, we simply change its state, not its identity.

```python
>>> lst1 = [1, 2, 3, 4]
>>> lst2 = lst1
>>> lst1.append(5)
>>> lst2
[1, 2, 3, 4, 5]
>>> lst1 is lst2
True
```

> You may think of the name in Python as the pointer variable in the C language, and the identity of an object in Python as the address of an object in the C language. In such an analogy:
>
> * assigning an object to a name is similar to assigning the address of this object to a pointer variable,
> * the `==` operator compares whether the two **pointed values** are the same,
> * and `is` operator compares whether the two **pointers** are the same.

You can use the built-in function `id` to fetch the identity of an object, which differs during different runnings of the Python interpreter. In fact, the expression `a is b` is equivalent to `id(a) == id(b)`.

```python
>>> lst = [1, 2, 3, 4]
>>> id(lst)
2624875298056 # It may be different on your machine
>>> lst.append(5)
>>> id(lst)
2624875298056
```
