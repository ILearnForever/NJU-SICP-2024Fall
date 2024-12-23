# Problem 3: Balanced Parentheses (100pts)

A parentheses sequence is a string consisting of left parenthesis `(` and right parenthesis `)`.

A parentheses sequence is balanced when every left parenthesis has a corresponding right parenthesis and the pairs of parentheses are properly nested. For example, `()` and `(())()` are balanced parentheses sequences, while `(` and `()()))` are not.

Formally, a parentheses sequence `s` is balanced if:

1. `s` is empty.
2. `s` starts with a `(`, ends with a `)`, and the rest part of `s` is balanced. For example, `()`.
3. `s` can be divided into two consecutive balanced parentheses sequence. For example, `()(())` is balanced since it can be divided into `()` and `(())`.

Write a recursive function `balanced` that takes a parentheses sequence `s` and returns whether `s` is balanced. For example, `balanced('()')` returns `True`, while `balanced(')')` and `balanced('(')` return `False`.

> _Hint1_: Read the docstring of the three given helper functions `divide`, `peel` and `match`, and try to make the best use of them.
>
> _Hint2_: Don't be afraid to use loops when you have to!

```python
def balanced(s):
    """Returns whether the given parentheses sequence s is balanced.
    >>> balanced('()')
    True
    >>> balanced(')')
    False
    >>> balanced('(())')
    True
    >>> balanced('()()')
    True
    >>> balanced('()())')
    False
    >>> balanced('()(()')
    False
    """

    def divide(s, k):
        """Divide the given parentheses sequence s into two parts at position k.
        >>> left, right = divide('()()', 2)
        >>> left
        '()'
        >>> right
        '()'
        >>> left, right = divide('(())()', 4)
        >>> left
        '(())'
        >>> right
        '()'
        >>> left, right = divide('(())()', 6)
        >>> left
        '(())()'
        >>> right
        ''
        """
        return (s[:k], s[k:])

    def peel(s):
        """Peel off the leftmost and rightmost parentheses in s to obtain the
        internal part of the parentheses sequence.
        >>> peel('(())')
        '()'
        >>> peel('()')
        ''
        >>> peel('))((')
        ')('
        """
        return s[1:-1]

    def match(s):
        """Returns whether the leftmost and the rightmost parentheses in s match.
        >>> match('()')
        True
        >>> match('()()')
        True
        >>> match('()))')
        True
        >>> match('))')
        False
        >>> match(')())')
        False
        """
        return s[0] == '(' and s[-1] == ')'

    "*** YOUR CODE HERE ***"
```
