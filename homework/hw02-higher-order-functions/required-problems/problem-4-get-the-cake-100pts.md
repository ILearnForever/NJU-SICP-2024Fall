# Problem 4: Get the Cake (100pts)

Nanami Chiaki heard that you are learning SICP and feel interested in high order functions. She designed the following missions to test your understanding. If you solve the missions correctly, Nanami will give you a "cake" as gift.

The `missions` function consists of three sub missions: `mission1`, `mission2` and `mission3`. The inner function `mission3_inner` returns a variable `cake`.

Your task is to write a higher order function so that it calls three mission functions in turn and return the hidden `cake`. Please note that you are not allowed to return variable `cake` or print the messages directly. **A correct solution contains only one expression.**

Wish you success!

```python
def missions(f):
    """DO NOT EDIT THIS FUNCTION"""
    def mission1(f):
        if f(0) == 0 and f(1) == 2:
            print('MISSION 1 SOLVED')
            return lambda g: mission2(g(f))
        else:
            print('MISSION 1 FAILED')

    def mission2(f):
        if f(0) == 0 and f(1) == 2:
            print('MISSION 2 SOLVED')
            return mission3(0, 0)
        else:
            print('MISSION 2 FAILED')

    def mission3(f, g):
        def mission3_inner(f):
            if f == g:
                return mission3(f, g + 1)

        if g == 5:
            print('MISSION 3 SOLVED')
            return 'The cake is a lie.'
        else:
            return mission3_inner

    return mission1(f)


def get_the_cake(missions):
    """
    Write a higher order function so that it calls three
    mission functions in turn and return the hidden cake.
    You are not allowed to return variable cake or print
    the messages directly. A correct solution contains
    only one expression.

    By the way, do you know that "The cake is a lie" is 
    a catchphrase from the 2007 video game Portal? Visit
    https://en.wikipedia.org/wiki/The_cake_is_a_lie
    if you have never played Portal before!

    >>> the_cake = get_the_cake(missions)
    MISSION 1 SOLVED
    MISSION 2 SOLVED
    MISSION 3 SOLVED
    >>> the_cake
    'The cake is a lie.'
    >>> # check that your answer consists of nothing but an
    >>> # expression (this docstring) and a return statement
    >>> import inspect, ast
    >>> [type(x).__name__ for x in ast.parse(inspect.getsource(get_the_cake)).body[0].body]
    ['Expr', 'Return']
    """
    return "*** YOUR CODE HERE ***"
```
