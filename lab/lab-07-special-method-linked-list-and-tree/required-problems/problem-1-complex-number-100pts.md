# Problem 1: Complex Number (100pts)

In mathematics, a complex number is a number that can be expressed in the form $$a+bi$$, where $$a$$𝑎 and $$b$$𝑏 are real numbers, and $$i$$𝑖 represents the imaginary unit that satisfies the equation $$i^2=−1$$. For example, $$2+3i$$ is a complex number. For the complex number $$a+bi$$, $$a$$ is called the real part, and $$b$$ is called the imaginary part. To emphasize, the imaginary part does not include a factor $$i$$; that is, the imaginary part is $$b$$, not $$bi$$.

Complex numbers can be added and multiplied. For any complex number $$c_1$$ and $$c_2$$ where $$c_1=a+bi$$ and $$c_2=c+di$$, the addition operator '+' is defined as $$c_1+c_2=(a+c)+(b+d)i$$ and the multiplication operator '⋅' is defined as $$c_1⋅c_2=(ac−bd)+(ad+bc)i$$.

Implement required methods of class `Complex` such that representing a `Complex` object `Complex(a, b)` displays `Complex(real=a, imaginary=b)`, printing it displays `a + bi` and we can directly add or multiply two complex objects.

```python
class Complex:
    """Complex Number.

    >>> a = Complex(1, 2)
    >>> a
    Complex(real=1, imaginary=2)
    >>> print(a)
    1 + 2i
    >>> b = Complex(-1, -2)
    >>> b
    Complex(real=-1, imaginary=-2)
    >>> print(b)
    -1 + -2i
    >>> print(a + b)
    0 + 0i
    >>> print(a * b)
    3 + -4i
    >>> print(a)
    1 + 2i
    >>> print(b)    # a and b should not be changed
    -1 + -2i
    """
    def __init__(self, real, imaginary):
        self.real = real
        self.imaginary = imaginary
    
    "*** YOUR CODE HERE ***"
```

> **Hint1**: You may find [Python string formatting syntax](https://docs.python.org/3/library/stdtypes.html#str.format) or [f-strings](https://docs.python.org/3/tutorial/inputoutput.html#fancier-output-formatting) useful. A quick example:
>
> ```
> >>> ten, twenty, thirty = 10, 'twenty', [30]
> >>> '{0} plus {1} is {2}'.format(ten, twenty, thirty)
> '10 plus twenty is [30]'
>
> >>> feeling = 'love'
> >>> year = 2024
> >>> course = 'SICP'
> >>> f'I {feeling} {course}-{year}!'
> 'I love SICP-2024!'
> ```
>
> **Hint2**: Some [special methods](https://docs.python.org/3/reference/datamodel.html#emulating-numeric-types) may help you achieve operator overloading.
