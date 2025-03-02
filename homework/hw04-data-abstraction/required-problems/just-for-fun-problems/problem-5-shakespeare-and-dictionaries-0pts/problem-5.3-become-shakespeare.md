# Problem 5.3: Become Shakespeare

Great! Now let's try to run our functions with some actual data. The following snippet included in the skeleton code will return a list containing the words in all of the works of Shakespeare.

```python
def shakespeare_tokens(url='https://www.composingprograms.com/shakespeare.txt'):
    """Return the words of Shakespeare's plays as a list."""
    from urllib.request import urlopen
    shakespeare = urlopen(url)
    return shakespeare.read().decode(encoding='ascii').split()

```

Uncomment the following two lines to run the above function and build the successors table from those tokens.

```python
# Uncomment the following two lines
# tokens = shakespeare_tokens()
# table = build_successors_table(tokens)
```

Next, let's define a utility function that constructs sentences from this successors table:

```python
>>> def sent():
...     return construct_sent('The', table)
>>> sent()
" The plebeians have done us must be news-cramm'd."

>>> sent()
" The ravish'd thee , with the mercy of beauty!"

>>> sent()
" The bird of Tunis , or two white and plucker down with better ; that's God's sake."
```

Notice that all the sentences start with the word "The". With a few modifications, we can make our sentences start with a random word. The following `random_sent` function (defined in your starter file) will do the trick:

```python
def random_sent():
    import random
    return construct_sent(random.choice(table['.']), table)

```

Go ahead and load your file into Python (be sure to use the -i flag). You can now call the `random_sent` function to generate random Shakespearean sentences!

```python
>>> random_sent()
" Long live by thy name , then , Dost thou more angel , good Master Deep-vow , And tak'st more ado but following her , my sight Of speaking false!"

>>> random_sent()
" Yes , why blame him , as is as I shall find a case , That plays at the public weal or the ghost.
```
