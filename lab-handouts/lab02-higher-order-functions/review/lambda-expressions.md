# Lambda Expressions

Lambda expressions are expressions that evaluate to functions by specifying two things: the parameters and a return expression.

```python
lambda <parameters>: <return expression>
```

While both `lambda` expressions and `def` statements create function objects, there are some notable differences. `lambda` expressions work like other expressions; much like a mathematical expression just evaluates to a number and does not alter the current environment, a `lambda` expression evaluates to a function without changing the current environment. Let's take a closer look.

|                           | **lambda**                                                                                                                                                    | **def**                                                                                                                                                            |
| ------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Type                      | _Expression_ that evaluates to a value                                                                                                                        | _Statement_ that alters the environment                                                                                                                            |
| Result of execution       | Creates an anonymous lambda function with no intrinsic name.                                                                                                  | Creates a function with an intrinsic name and binds it to that name in the current environment.                                                                    |
| Effect on the environment | Evaluating a `lambda` expression does _not_ create or modify any variables.                                                                                   | Executing a `def` statement both creates a new function object _and_ binds it to a name in the current environment.                                                |
| Usage                     | A `lambda` expression can be used anywhere that expects an expression, such as in an assignment statement or as the operator or operand to a call expression. | After executing a `def` statement, the created function is bound to a name. You should use this name to refer to the function anywhere that expects an expression. |

*   **lambda** example

    ```python
    # A lambda expression by itself does not alter
    # the environment
    lambda x: x * x

    # We can assign lambda functions to a name
    # with an assignment statement
    square = lambda x: x * x
    square(3)

    # Lambda expressions can be used as an operator
    # or operand
    negate = lambda f, x: -f(x)
    negate(lambda x: x * x, 3)

    # We can directly call a lambda expression
    # just created
    # Make sure the lambda expression wrapped in a
    # pair of parenthesis or between `(`, `,`, and `)`
    # in order not to let Python misunderstand you
    (lambda x: x * 2 ** x)(5) # evaluates to 160
    ```
*   **def** example

    ```python
    def square(x):
        return x * x

    # A function created by a def statement
    # can be referred to by its intrinsic name
    square(3)
    ```
