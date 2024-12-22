# 作业文件

操作

从课程主页下载本次实验所需的文件。

对于本次实验而言是 `lab00-Code.zip` 这个压缩包。

## 解压 <a href="#jie-ya" id="jie-ya"></a>

下载到电脑里的实验文件需要解压后使用。我们推荐为每个实验建立一个单独的文件夹以方便后续的管理。 Windows 下的解压可以参照[这篇文章的内容](https://support.microsoft.com/zh-cn/windows/%E5%8E%8B%E7%BC%A9%E5%92%8C%E8%A7%A3%E5%8E%8B%E7%BC%A9%E6%96%87%E4%BB%B6-f6dde0a7-0fec-8294-e1d3-703ed85e7ebc)。

操作

解压下载完成的 `lab00-Code.zip` 文件，得到 `lab00-Code` 文件夹。

## 用 VSCode 打开 <a href="#yong-vscode-da-kai" id="yong-vscode-da-kai"></a>

操作

用 VSCode 打开解压完毕的 `lab00-Code` 文件夹。

打开刚刚解压到的文件夹，右键点击一处空白区域，再选择【用Code打开】。这样操作相当于用VSCode打开整个文件夹，这对后面的实验会比较方便。

![](https://sicp.pascal-lab.net/2024/labs/lab00/images/open_vscode.png)

为什么我找不到这个选项？

请检查：

1. 右键菜单中的“显示更多选项”。
2. VSCode 安装时选项是全部否勾选。

## Hello, Code! <a href="#hello-code" id="hello-code"></a>

本次实验的作业文件是`lab00.py`。 打开`lab00.py`，首先能看到下面这段代码：

```python
def twenty_twenty_four():
    """Come up with the most creative expression that evaluates to 2024,
    using only numbers and the +, *, and - operators.

    >>> twenty_twenty_four()
    2024
    """
    return ______
```

操作

阅读并尝试理解 `hello.py` 中的内容。

上面代码里包含了我们将要完成的第一个题目——2024（这个题目就叫做2024）。看到上面的代码时，你可能是一脸懵逼的。不过不要慌，我们来一步一步理解。

首先，这段代码使用`def twenty_twenty_four()`定义了一个函数`twenty_twenty_four()`。

还没学到这里？

如果在实验课前老师还没讲如何定义函数，大家也不用着急，不知道这个知识点也能完成本次实验。 不过，在下一次课上你应该就会学到如何定义函数了。

接下来，我们会看到一段被三引号 `"""` 包围的文本，我们把这段文本叫做 docstring（全称 document string，即文档字符串），它一般被用来描述一个函数应该做什么。对于 python 来说，这段文本就是一&#x6BB5;_&#x6CE8;释_（Comment）而已，并不会被执行。

在 `twenty_twenty_four` 的例子中，这段 docstring 告诉我们：“**写出一个富有创造力的表达式，使得计算它的值能得到 2024**”（当然，在本次实验中没那么有创造力也无妨）。此外，它还要求我们“**只可以使用数字、加法、乘法和减法**”。

紧接着，我们能看到有一行 docstring 是以 `>>>` 开头的。从这行开始往下的 docstring 被叫做doctest (举一反三一下，它的全称为什么？——document test)。回想一下大家在前面使用的 Python 交互模式，`>>>` 被我们称为提示符——它告诉我们可以在它后面输入表达式或者语句。是不是当你在 `>>>` 后面输入一个表达式后，Python 解释器就会在下一行打印这个表达式的值？doctest 就是通过这样的示例来告诉你一个函数会做什么：“当我们在交互模式下这样输入代码，就会得到这样的结果”。

在我们 `twenty_twenty_four` 的例子中，doctest 告诉我们：“当我们在交互模式下输入 `twenty_twenty_four()`，就会得到 2024”。

总的来说，docstring 和 doctest 分别使用“描述”和“举例”的手段来告诉我们一个函数的行为。未来在大家完成实验题目的时候，除了阅读实验讲义，也最好读一读它们加深自己的理解。
