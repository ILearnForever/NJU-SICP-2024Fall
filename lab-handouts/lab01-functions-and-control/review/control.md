# Control

## **Boolean Operators**

Python supports three boolean operators: `and`, `or`, and `not`:

```python
>>> True and True
True
>>> True and False
False
>>> True or False
True
>>> not True
False
>>> a = 4
>>> a < 2 and a > 0
False
>>> a < 2 or a > 0
True
>>> not (a > 0)
False
```

* `and` evaluates to `True` if both of its operands evaluate to `True`. If at least one operand is `False`, then `and` evaluates to `False`.
* `or` evaluates to `True` if at least one operand evaluates to `True`. If both operands are `False`, then `or` evaluates to `False`.
* `not` evaluates to `True` if its operand evaluates to `False`. It evaluates to `False` if its operand evaluates to `True`.

What do you think the following expression evaluates to? Try it out in your Python interpreter.

```python
>>> True and not False or not True and False
```

It is difficult to read complex expressions, like the one above, and understand how a program will behave.

What about this one?

```python
>>> 1 * -0 + -1 * 0
```

As is explained in lab00, using parentheses can make your code easier to understand. Python interprets that complex boolean expression in the following way:

```python
>>> (True and (not False)) or ((not True) and False)
```

This is because boolean operators, like arithmetic operators, have precedence:

* `not` has the highest priority, similar to negation
* `and` is much like multiplication
* `or` has the lowest priority, similar to subtraction

**Truthy and Falsey Values**: It turns out `and` and `or` work on more than just booleans (`True`, `False`). Python values such as `0`, `None`, `''` (the empty string), and `[]` (the empty list) are considered false values. _**All other values**_ are considered true values.

{% hint style="info" %}
How to prove it?
{% endhint %}

## **Short Circuiting**

What do you think will happen if we type the following into Python?

```python
1 / 0
```

Try it out in Python! You should see a `ZeroDivisionError`. But what about this expression?

```python
True or 1 / 0
```

It evaluates to `True` because `and` and `or` operators in Python _**short-circuit**_. That is, they don't necessarily evaluate every operand.

<table><thead><tr><th align="center">Operator</th><th align="center">Checks if:</th><th width="297" align="center">Evaluates from left to right up to:</th><th align="center">Example</th></tr></thead><tbody><tr><td align="center">AND</td><td align="center">All values are true</td><td align="center">The first false value</td><td align="center"><code>False and 1 / 0</code> evaluates to <code>False</code></td></tr><tr><td align="center">OR</td><td align="center">At least one value is true</td><td align="center">The first true value</td><td align="center"><code>True or 1 / 0</code> evaluates to <code>True</code></td></tr></tbody></table>

Short-circuiting happens when the evaluation of the expression reaches an operand that allows Python to make a conclusion about the expression. For example, `and` will short-circuit as soon as it reaches the first false value because it then knows the expression cannot be true since not all the operands are true.

If `and` and `or` do not _short-circuit_, they just return the last value; another way to remember this is that `and` and `or` always return the last thing they evaluate, whether they short circuit or not. Keep in mind that `and` and `or` don't always return booleans when using values other than `True` and `False`.

{% hint style="info" %}
Can you explain what `[] and True` evaluates to and why?
{% endhint %}

## **If Statements**

You can review the syntax of `if` statements in [Section 1.5.4](http://www.composingprograms.com/pages/15-control.html#conditional-statements) of Composing Programs.

{% hint style="info" %}
We sometimes see code that looks like this:

```python
if x > 3:
    return True
else:
    return False
```

This can be written more concisely as `return x > 3`. If your code looks like the code above, see if you can rewrite it more clearly!
{% endhint %}

## **While Loops**

You can review the syntax of `while` loops in [Section 1.5.5](http://www.composingprograms.com/pages/15-control.html#iteration) of Composing Programs.
