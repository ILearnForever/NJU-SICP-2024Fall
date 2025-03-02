# Generators

We can create our own custom iterators by writing a _generator_ function, which returns a special type of iterator called a **generator**. Generator functions have `yield` statements within the body of the function instead of `return` statements. Calling a generator function will return a generator object and will _not_ execute the body of the function.

For example, let's consider the following generator function:

```python
def countdown(n):
    print("Beginning countdown!")
    while n >= 0:
        yield n
        n -= 1
    print("Blastoff!")
```

Calling `countdown(k)` will return a generator object that counts down from `k` to `0`. Since generators are iterators, we can call `iter` on the resulting object, which will simply return the same object. Note that the body is not executed at this point; nothing is printed and no numbers are output.

```python
>>> c = countdown(5)
>>> c
<generator object countdown ...>
>>> c is iter(c)
True
```

So how is the counting done? Again, since generators are iterators, we call `next` on them to get the next element! The first time `next` is called, execution begins at the first line of the function body and continues until the `yield` statement is reached. The result of evaluating the expression in the `yield` statement is returned. The following interactive session continues from the one above.

```python
>>> next(c)
Beginning countdown!
5
```

Unlike functions we've seen before in this course, generator functions can remember their state. On any consecutive calls to `next`, execution picks up from the line after the `yield` statement that was previously executed. Like the first call to `next`, execution will continue until the next `yield` statement is reached. Note that because of this, `Beginning countdown!` doesn't get printed again.

```python
>>> next(c)
4
>>> next(c)
3
```

The next 3 calls to `next` will continue to `yield` consecutive descending integers until `0`. On the following call, a `StopIteration` error will be raised because there are no more values to `yield` (i.e. the end of the function body was reached before hitting a `yield` statement).

```python
>>> next(c)
2
>>> next(c)
1
>>> next(c)
0
>>> next(c)
Blastoff!
StopIteration
```

Separate calls to `countdown` will create distinct generator objects with their own state. Usually, generators shouldn't restart. If you'd like to reset the sequence, create another generator object by calling the generator function again.

```python
>>> c1, c2 = countdown(5), countdown(5)
>>> c1 is c2
False
>>> next(c1)
Beginning countdown!
5
>>> next(c2)
Beginning countdown!
5
```

Here is a summary of the above:

* A generator function has a `yield` statement and returns a _generator object_.
* Calling the `iter` function on a generator object returns the same object without modifying its current state.
* The body of a generator function is not evaluated until `next` is called on a resulting generator object. Calling the `next` function on a generator object computes and returns the next object in its sequence. If the sequence is exhausted, `StopIteration` is raised.
* A generator "remembers" its state for the next `next` call. Therefore,
  * The first `next` call works like this:
    * Enter the function and run until the line with `yield`.
    * Return the value in the `yield` statement, but remember the state of the function for future `next` calls.
  * And subsequent `next` calls work like this:
    * Re-enter the function, start at **the line after the `yield` statement that was previously executed**, and run until the next `yield` statement.
    * Return the value in the `yield` statement, but remember the state of the function for future `next` calls.
* Calling a generator function returns a brand new generator object (like calling `iter` on an iterable object).
* A generator should not restart unless it's defined that way. To start over from the first element in a generator, just call the generator function again to create a new generator.

Another useful tool for generators is the `yield from` statement (introduced in Python 3.3). `yield from` will yield all values from an iterator or iterable.

```python
>>> def gen_list(lst):
...     yield from lst
...
>>> g = gen_list([1, 2, 3, 4])
>>> next(g)
1
>>> next(g)
2
>>> next(g)
3
>>> next(g)
4
>>> next(g)
StopIteration
```
