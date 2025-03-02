# Lists

List is a Python data structure that can store multiple elements. Each element can be any type and can even be another list! A list is written as a comma separated list of expressions within a pair of square brackets:

```python
>>> list_of_nums = [1, 2, 3, 4]
>>> list_of_bools = [True, True, False, False]
>>> nested_lists = [1, [2, 3], [4, [5]]]
```

Each element in a list has an _index_. Lists are zero-indexed, meaning their indices start at 0 and increase in sequential order. To retrieve an element from a list, we can use list indexing:

```python
>>> lst = [6, 5, 4, 3, 2, 1]
>>> lst[0]
6
>>> lst[3]
3
```

Often times we need to know how long a list is when we're working with it. To find the length of a list, we can call the function `len`:

```python
>>> len([])
0
>>> len([2, 4, 6, 8, 10])
5
```

> Tip: Recall that empty lists, \[], are falsy values. Therefore, you can use an if statement like the following if you only want to do operations on non-empty lists:
>
> ```python
> if lst:
>  # Do stuff with the elements of list
> ```
>
> This is equivalent to:
>
> ```python
> if len(lst) > 0:
>  # Do stuff
> ```

You can also create a copy of a portion of the list using list slicing. To slice a list, use the syntax: `lst[<start index>:<end index>]`. This expression evaluates to a new list containing the elements of `lst` starting at the element at `<start index>` (inclusive) up to the element at `<end index>` (exclusive).

```python
>>> lst = [1, 2, 3, 4, 5]
>>> lst[1:4] # Starting from index 1 (inclusive) to 4 (exclusive)
[2, 3, 4]
>>> lst[:3]  # Start index defaults to 0
[1, 2, 3]
>>> lst[3:]  # End index defaults to len(lst)
[4, 5]
>>> lst[:]   # Creates a copy of the whole list
[1, 2, 3, 4, 5]
>>> lst[4:3] # What happens when start index is greater than end index
[]
```
