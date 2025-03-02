# Problem 9: Insert (100pts)

Write a function `insert_items` which takes as input a list `lst`, an argument `entry`, and another argument `elem`.

This function will check through each item present in `lst` to see if it is equivalent with `entry`. Upon finding an equivalent entry, the function should modify the list by placing `elem` into the list right after the found entry.

At the ending of the function, the modified list should be returned.

See the doctests for examples about the usage of this function. Use list mutation to modify the original list, no new lists should be created or returned.

**Be careful in situations where the values passed into entry and elem are equivalent, so as not to create an infinitely long list while iterating through it.** If you find that your code is taking more than a few seconds to run, it is most likely that the function is in a loop of inserting new values.

```python
def insert_items(lst, entry, elem):
    """
    >>> test_lst = [1, 5, 8, 5, 2, 3]
    >>> new_lst = insert_items(test_lst, 5, 7)
    >>> new_lst
    [1, 5, 7, 8, 5, 7, 2, 3]
    >>> large_lst = [1, 4, 8]
    >>> large_lst2 = insert_items(large_lst, 4, 4)
    >>> large_lst2
    [1, 4, 4, 8]
    >>> large_lst3 = insert_items(large_lst2, 4, 6)
    >>> large_lst3
    [1, 4, 6, 4, 6, 8]
    >>> large_lst3 is large_lst
    True
    """
    "*** YOUR CODE HERE ***"

```

> _Hint_: You may use the `lst.insert(ind, obj)` to insert an element `obj` to a position indexed by `ind`. Search the internet for more information about its usage. Here is just [a reference from Python Documentation](https://docs.python.org/3.11/tutorial/datastructures.html#more-on-lists).
