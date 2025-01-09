# Error Messages

By now, you've probably seen a couple of error messages. They might look intimidating, but error messages are very helpful for debugging. The following are some common types of errors:

|    Error Types    |                                                                 Descriptions                                                                 |
| :---------------: | :------------------------------------------------------------------------------------------------------------------------------------------: |
|    SyntaxError    |              Contained improper syntax (e.g. missing a colon after an `if` statement or forgetting to close parentheses/quotes)              |
|  IndentationError |                               Contained improper indentation (e.g. inconsistent indentation of a function body)                              |
|     TypeError     | Attempted operation on incompatible types (e.g. trying to add a function and a number) or called function with the wrong number of arguments |
| ZeroDivisionError |                                                          Attempted division by zero                                                          |

Using these descriptions of error messages, you should be able to better understand what went wrong with your code. **If you run into error messages, try to identify the problem yourself before asking for help.** You can always Google unfamiliar error messages to check their meaning and see if others have made similar mistakes.

For example:

```python
>>> def square(x):
...     return x * x
...
>>> square(2024, 2024)
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: square() takes 1 positional argument but 2 were given
```

Note:

* The last line of an error message tells us the type of the error. In the example above, we have a `TypeError`.
* The error message tells us what we did wrong -- we gave `square` 2 arguments but it can only take in 1 argument. In general, the last line of an error message is the most helpful.
* The second to last line of the error message tells us where the error occurred, which helps us track down the error. In the example above, `TypeError` occurred at `line 1` since we are in interactive mode.
