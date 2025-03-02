# Functions

It is common to write some code over and over again during programming. Let's say we want to know the _BMI_(Body Mass Index) of a given person. The formula is given by

$$BMI=mh2$$BMI=𝑚ℎ2

Where $$m$$𝑚 stands for weight (in kilograms) and $$h$$ℎ stands for height (in meters).

For a person who's 1.7 meters tall and weighs 70 kilograms, one way to tell his/her BMI is as follows:

```python
>>> 70 / (1.7 * 1.7)
24.221453287197235
```

According to Python, his/her BMI would be `24.221453287197235`.

Say, if TAs of SICP need to know the BMI of all the students (more than 200!) in the class, then they will have to do something like this:

```python
>>> 70 / (1.7 * 1.7)
24.221453287197235
>>> 60 / (1.6 * 1.6)
23.4375
>>> 80 / (1.8 * 1.8)
24.691358024691358
...
```

Code above introduces _duplications_ (i.e., height appears twice in every expression). For more than 200 students, such duplication may lead to bugs as TAs might accidentally get someone's height wrong for its second appearance:

```python
>>> 70 / (1.7 * 1.6) # Wrong!
25.735294117647058
```

To capture the essence of calculating one's BMI using his/her weight and height, we can instead write a function for the (possibly exhausted) TAs:

```python
def BMI(h, m):
    return m / (h * h)
```

This function, called `BMI`, takes in two **arguments**, the height `h` and weight `m` of a person, and will **return** the BMI of that person, using the formula mentioned above. It provides an _abstraction_ for BMI calculation so that programmers can reuse some code fragments without typing the formula again and again.

Now we can **call** this function whenever we want to calculate the BMI if given height and weight. Applying a function to some expressions is done with a **call expression**.

```python
>>> BMI(1.7, 70)
24.221453287197235
>>> BMI(1.6, 60)
23.4375
>>> BMI(1.8, 80)
24.691358024691358
```

TAs can now take some rest thanks to your help.

[**2.1.1 Call expressions**](https://sicp.pascal-lab.net/2024/labs/lab01/2_1.html#211-call-expressions)

A call expression applies a function, which may or may not accept arguments, to zero or more expressions. The call expression evaluates to the function's return value.

The syntax of a function call:

```
  add   (    2   ,    3   )
   |         |        |
operator  operand  operand
```

Every call expression requires a set of parentheses delimiting its comma-separated operands. We refer to the function being called as the **operator**, and the expressions surrounded by parentheses as the **operands**.

To evaluate a call expression:

1. Evaluate the operator (i.e., the function), and then the operands (from left to right).
2. Apply the operator to the operands (the values of the operands).

If an operand in a call expression is itself a call expression (.e.g, `BMI(1.7, BMI(1.7, 70))`), then these two steps are applied to that inner operand first in order to evaluate the entire expression.

[**2.1.2 `return` and `print`**](https://sicp.pascal-lab.net/2024/labs/lab01/2_1.html#212-return-and-print)

Most functions that you define will contain a `return` statement. The `return` statement will give the result of some computation back to the caller of the function and exit the function. For example, the function `square` below takes in a number `x` and returns the square of `x`.

```python
def square(x):
    """
    >>> square(4)
    16
    """
    return x * x
```

When Python executes a `return` statement, the function containing that `return` statement terminates immediately. If Python reaches the end of the function body without executing a `return` statement, it will automatically return `None`.

In contrast, the `print` function is used to display values in the Terminal. This can lead to some confusion between `print` and `return` because calling a function in the Python interpreter will print out the function's return value.

However, unlike a `return` statement, when Python evaluates a `print` expression, the function does _not_ terminate immediately.

```python
def what_prints():
    print('Hello World!')
    return 'Exiting this function.'
    print('61A is awesome!')

>>> what_prints()
Hello World!
'Exiting this function.'
```

> Notice also that `print` displays text without quotes, but `return` preserves them.
