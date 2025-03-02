# Problem 4: Reverse (50pts)

`my_reverse` takes in a list `l` and returns a new list that contains exactly the same elements in `l` but in the reverse order.

> _Hint_: use clever slicing.

```python
def my_reverse(l):
    """Returns a new list that contains the exact same elements in l with reversed order.
    >>> a = ['S', 'I', 'C', 'P']
    >>> a is my_reverse(a) # the returned list is newly created
    False
    >>> my_reverse(my_reverse(a)) == a # reverse twice equals to the original list
    True
    >>> my_reverse(a)
    ['P', 'C', 'I', 'S']
    >>> a
    ['S', 'I', 'C', 'P']
    """
    "*** YOUR CODE HERE ***"
```
