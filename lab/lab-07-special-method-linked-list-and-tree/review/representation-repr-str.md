# Representation: Repr, Str

There are two main ways to produce the "string" of an object in Python: `str()` and `repr()`. While the two are similar, they are used for different purposes.

`str()` is used to describe the object to the end user in a "Human-readable" form, while `repr()` can be thought of as a "Computer-readable" form mainly used for debugging and development.

When we define a class in Python, `__str__` and `__repr__` are both built-in methods for the class.

We can call those methods using the global built-in functions `str(obj)` or `repr(obj)` instead of dot notation, `obj.__repr__()` or `obj.__str__()`.

In addition, the `print()` function calls the `__str__` method of the object, while simply calling the object in interactive mode calls the `__repr__` method.

Here's an example:

```python
class Rational:

    def __init__(self, numerator, denominator):
        self.numerator = numerator
        self.denominator = denominator

    def __str__(self):
        return f'{self.numerator}/{self.denominator}'

    def __repr__(self):
        return f'Rational({self.numerator},{self.denominator})'
```

```
>>> a = Rational(1, 2)
>>> str(a)
'1/2'
>>> repr(a)
'Rational(1,2)'
>>> print(a)
1/2
>>> a
Rational(1,2)
```

### [(Optional) Special Methods](https://sicp.pascal-lab.net/2024/labs/lab07/2_1.html#optional-special-methods) <a href="#optional-special-methods" id="optional-special-methods"></a>

For those who are really interested in special methods, you can visit the following sites:

* [Section 2.7.2](https://www.composingprograms.com/pages/27-object-abstraction.html#special-methods)
* [Python official doc about special method names](https://docs.python.org/3.9/reference/datamodel.html#special-method-names)
