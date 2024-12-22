# 写点代码

现在，我们应该理解了作业文件中的第一个题目，即写一个（有创造力的）表达式，使得它的值为`2024`。

那么我们该把这个表达式写在哪里呢？我们的实验讲义会把这种要求都描述清楚。本次实验其它题目的描述可以在左侧的“本次实验内容”一节中找到。作为一个带大家一起做的例子，我们现在先告诉大家第一个题目的要求：**请用你想到的那个表达式替换掉`twenty_twenty_four`中下划线的部分**。

当然，我们之前说过第一个题目我们会带大家一起做。所以虽然不知道富有创造力的大家想到了什么表达式，但没有创造力的助教们就想了一个这样的答案：

```python
def twenty_twenty_four():
    """Come up with the most creative expression that evaluates to 2024,
    using only numbers and the +, *, and - operators.

    >>> twenty_twenty_four()
    2024
    """
    return 2025 - 1
```

助教也试着让 ChatGPT 做做这道题目，它给出的答案是这样的：

```python
# Here’s a fun and creative way to generate the number 2024 using just numbers and the `+`, `*`, and `-` operators:

def twenty_twenty_four():
    """Come up with the most creative expression that evaluates to 2024,
    using only numbers and the +, *, and - operators.

    >>> twenty_twenty_four()
    2024
    """
    return (2000 * 1) + (2 * 12)

# Explanation:
# - We use `2000 * 1` to generate 2000.
# - Then, we add `(2 * 12)` to generate 24.
# - The sum results in `2024`.

# This adheres to the constraints while using a little bit of creative multiplication and addition!
```

大家可以修改各自得到的`lab00.py`文件，把下划线替换成自己想到的表达式。

操作

把下划线替换成自己想到的表达式，并保存文件。
