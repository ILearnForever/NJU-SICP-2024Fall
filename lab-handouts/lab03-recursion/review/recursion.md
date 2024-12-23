# Recursion

A recursive function is a function that calls itself in its body, either directly or indirectly. Recursive functions have three important components:

1. Base case(s), the simplest possible form of the problem you're trying to solve.
2. Recursive case(s), where the function calls itself with a **simpler argument** as part of the computation.
3. Combining results from recursive calls to solve the full problem.

> Q: What does "**simpler**" mean?
>
> A: Well, for integer `i` and `j`, `i` is **simpler** than `j` _iff_ `i < j`
>
> Q: So, "**simpler**" means less than?
>
> A: "Generalized" less than. This can be tricky for some problems, see [Problem 1](https://sicp.pascal-lab.net/2024/labs/lab03/5_1.html).

Let's look at the canonical example, `factorial`.

> Factorial, denoted with the ! operator, is defined as:
>
> $$n!=∏i=1ni=n×(n−1)×⋯×1$$𝑛!=∏𝑖=1𝑛𝑖=𝑛×(𝑛−1)×⋯×1Or, equivalently, in a recursive way:$$n!={1n×(n−1)!n=0otherwise$$𝑛!={1𝑛=0𝑛×(𝑛−1)!otherwiseFor example:$$5!=5×4×3×2×1=120$$5!=5×4×3×2×1=120

An iterative _implementation_ for factorial might look like this:

```python
def factorial(n):
    result, i = 1, 1
    while i <= n:
        result = result * i
        i += 1
    return result
```

In contrast, a recursive _implementation_ for factorial is as follows, note how it resembles the recursive _definition_ of factorial:

```python
def factorial(n):
    if n == 0:
        return 1
    else:
        return n * factorial(n - 1)
```

1. Base case: by the definition of factorial, the simplest possible form would be `0!` since `n == 0` is the smallest number we can compute the factorial of.
2. Recursive case: follows immediately from the definition of factorial, i.e., `factorial(n) = n * factorial(n - 1)`, where `factorial(n - 1)` is a recursive call to `factorial` with a simpler argument `n - 1`.
3. Combining results: as for factorial, simply multiply `factorial(n - 1)` by `n` and return the result.

In this lab you will be implementing recursive functions to solve some problems. Here are some general tips:

* Paradoxically, to write a recursive function, you must assume that the function is fully functional before you finish writing it; this is called the recursive leap of faith.
* Consider how you can solve the current problem using the solution to a simpler version of the problem. The amount of work done in a recursive function can be deceptively little: remember to take the leap of faith and trust the recursion to solve the slightly smaller problem without worrying about how.
* Think about what the answer would be in the simplest possible case(s). These will be your base cases - the stopping points for your recursive calls. Make sure to consider the possibility that you're missing base cases (this is a common way recursive solutions fail).
* It may help to write an iterative version first.
