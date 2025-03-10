# Environment Diagrams

Environment diagrams are one of the best learning tools for understanding `lambda` expressions and higher order functions because you're able to keep track of all the different names, function objects, and arguments to functions. We highly recommend drawing environment diagrams or using [Python tutor](http://pythontutor.com/composingprograms.html) if you get stuck doing the WWPD problems below. For examples of what environment diagrams should look like, try running some code in Python tutor. Here are the rules:

## Assignment Statements <a href="#id-241-assignment-statements" id="id-241-assignment-statements"></a>

1. Evaluate the expression on the right hand side of the `=` sign.
2. If the name found on the left hand side of the `=` doesn't already exist in the current frame, write it in. If it does, erase the current binding. Bind the _value_ obtained in step 1 to this name.

If there is more than one name/expression in the statement, evaluate all the expressions first from left to right before making any bindings.

Try to paste the following code in the [Python tutor](http://pythontutor.com/composingprograms.html) and understand each execution step. You can also click this [link](http://pythontutor.com/composingprograms.html#code=x%20%3D%2010%0Ay%20%3D%20x%0Ax%20%3D%2.40%0Ax,%20y%20%3D%20y%20%2B%201,%20x%20-%201\&cumulative=true\&curInstr=0\&mode=display\&origin=composingprograms.js\&py=3\&rawInputLstJSON=%5B%5D).

```python
x = 10
y = x
x = 20
x, y = y + 1, x - 1
```

## Def Statements <a href="#id-242-def-statements" id="id-242-def-statements"></a>

1. Draw the function object with its intrinsic name, formal parameters, and parent frame. A function's parent frame is the frame in which the function was defined.
2. If the intrinsic name of the function doesn't already exist in the current frame, write it in. If it does, erase the current binding. Bind the newly created function object to this name.

Try to paste the following code in the [Python tutor](http://pythontutor.com/composingprograms.html) and understand each execution step. You can also click this [link](http://pythontutor.com/composingprograms.html#code=def%20f%28x%29%3A%0A%20%20%20%20return%20x%20%2B%201%0A%0Adef%20g%28y%29%3A%0A%20%20%20%20return%20y%20-%201%0A%0Adef%20f%28z%29%3A%0A%20%20%20%20return%20x%20*%2.4\&cumulative=true\&curInstr=0\&mode=display\&origin=composingprograms.js\&py=3\&rawInputLstJSON=%5B%5D).

```python
def f(x):
    return x + 1

def g(y):
    return y - 1

def f(z):
    return x * 2
```

## Call Expressions <a href="#id-243-call-expressions" id="id-243-call-expressions"></a>

{% hint style="info" %}
you do not have to go through this process for a built-in Python function like `max` or `print`.
{% endhint %}

1. Evaluate the operator, whose value should be a function.
2. Evaluate the operands left to right.
3. Open a new frame. Label it with the sequential frame number, the intrinsic name of the function, and its parent.
4. Bind the formal parameters of the function to the arguments whose values you found in step 2.
5. Execute the body of the function in the new environment.

Try to paste the following code in the [Python tutor](http://pythontutor.com/composingprograms.html) and understand each execution step. You can also click this [link](http://pythontutor.com/composingprograms.html#code=def%20f%28a,%20b,%20c%29%3A%0A%20%20%20%20return%20a%20*%20%28b%20%2B%20c%29%0A%0Adef%20g%28x%29%3A%0A%20%20%20%20return%203%20*%20x%0A%0Af%281%20%2B%2.4,%20g%2.4%29,%206%29\&cumulative=true\&curInstr=0\&mode=display\&origin=composingprograms.js\&py=3\&rawInputLstJSON=%5B%5D).

```python
def f(a, b, c):
    return a * (b + c)

def g(x):
    return 3 * x

f(1 + 2, g(2), 6)
```
