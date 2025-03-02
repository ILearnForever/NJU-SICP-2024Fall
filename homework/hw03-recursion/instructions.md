# Instructions

In this homework, you are required to complete the problems described in section 2. The starter code for these problems is provided in `hw03.py`, which is distributed as part of the homework materials in the `code` directory.

We have also prepared two optional problems just for fun in section 3. You can find further descriptions there.

**Submission**: As instructed before, you need to submit your work with Ok by `python ok --submit`. You may submit more than once before the deadline, and your score of this assignment will be the highest one of all your submissions.

**Readings**: You might find the following references to the textbook useful:

* [Section 1.7](http://www.composingprograms.com/pages/17-recursive-functions.html)

> The `construct_check` module in `construct_check.py` is used in this assignment, which defines the function check. For example, a call such as
>
> ```python
> check("foo.py", "func1", ["While", "For", "Recursion"])
> ```
>
> checks that the function `func1` in file `foo.py` does not contain any while or for constructs, and is not an overtly recursive function (i.e., one in which a function contains a call to itself by name). Note that this restriction does not apply to all problems in this assignment. If this restriction applies, you will see a call to check somewhere in the problem's doctests.
