# 我实现的对不对？

现在，大家已经完成了第一个题目。这个题目当然是很简单的，但之后随着知识的增多，我们要完成的题目也越发复杂。那么有没有什么方法能检验我们写的代码对不对呢？

## 手动测试代码 <a href="#shou-dong-ce-shi-dai-ma" id="shou-dong-ce-shi-dai-ma"></a>

回想一下，doctest描述了“当我们在交互模式下这样输入代码，就会得到这样的结果”，那么我们是不是可以打开交互模式，按照doctest的描述输入代码，然后观察结果是不是一致的呢？

是的！我们可以打开一个交互模式的 python，然后把作业文件粘贴进去，最后按一下回车，python就把文件的代码运行完了。然后，我们就可以对照着 doctest 输入 doctest 即可测试：

```python
$ python
>>> def twenty_twenty_four():
...     """Come up with the most creative expression that evaluates to 2024,
...     using only numbers and the +, *, and - operators.
...
...     Expected result:
...     >>> twenty_twenty_four()
...     2024
...     """
...     return 2024
...
>>>
>>> def sum(a, b):
...     """Compute the sum of a and b.
...
...     Expected result:
...     >>> sum(1, 2)
...     3
...     >>> sum(3, 8)
...     11
...     """
...     return ______
...
>>>
>>> def diff_square(a, b):
...     """Compute the difference of square a and square b.
...
...     Expected result:
...     >>> diff_square(3, 2)
...     5
...     >>> diff_square(3, 4)
...     -7
...     """
...     return ______
...
>>> twenty_twenty_four()
2024
```

这和doctest描述的一模一样，所以你现在可以松口气，相信自己的代码是对的了。如果发现不一样，你就需要看看自己哪里出问题了。

操作

启动 python 的交互模式，把文件 `lab00.py` 中的全部内容复制进去后，执行 `twenty_twenty_four()` 以查看结果。

等一等

刚才其实有一个概念的陷阱。现在让我们思考一个问题：为什么说，经过刚才这样一个过程，我们就有理由相信我们的代码是对的呢？

实际上，“相信自己的代码是对的”是一个错误的说法！准确的说，大家只能有理由相信“自己写的代码和doctest所预期的相符合”，进而推论，自己的代码**可能**是对的。

其实，像这样一个比较代码的实际执行结果和预期结果的过程就叫&#x505A;_&#x6D4B;试_（Testing）。这也是“doctest”中test的中文含义。

测试**不能保证**代码是对的，只能保证代码在多大程度上与预期相符合。但如果通过了足够多、足够复杂的测J试，我们就更加有信心，更容易相信我们的代码是对的。 反过来讲，如果代码连基本的测试都没有通过，说明肯定不是对的。

有没有更好的保证正确性的办法？

当然有！

* _形式化验证_（Formal Verification），通过逻辑和推理规则（而非一个一个的测试样本）来证明程序的正确性。这种技术在涉及生命财产安全的领域有更广泛的运用。
* _静态分析_（Static Analysis），通过抽象和近似来确保程序的安全性。这种技术在当今流行的 IDE、代码编辑器和编译器中都有广泛的运用。

## 使用Ok进行自动化测试 <a href="#shi-yong-ok-jin-xing-zi-dong-hua-ce-shi" id="shi-yong-ok-jin-xing-zi-dong-hua-ce-shi"></a>

随着大家做的题目越来越多、越来越复杂，同学们可能会发现，每当自己写了一段新的代码，就要重新走上面一套doctest的流程，这样会非常麻烦。

程序员都是懒惰的生物，嫌麻烦是人类的天性，这也是为什么我们要开发各种各样的减轻负担的工具。 为了减轻同学们测试的负担，tygg 开发了 SICP 插件。在前面的章节中我们也介绍了插件的安装。

操作

点击函数 `twenty_twenty_four` 上的 `Run` 按钮以测试你的代码。

![](https://sicp.pascal-lab.net/2024/labs/lab00/images/vsc-sicp.png)

什么是 Debug？

Debug就是修复代码中的缺陷（bug）。Debug模式下，我们可以让代码一步一步地执行，或者是查看各个变量的中间值。

登陆？

> **为什么我点击`Run`（或者`Debug`）打开了浏览器，访问了南京大学代码托管系统？**

Ok不仅是一个测试工具，我们还需要用它提交作业。 提交作业时，我们通过南京大学代码托管系统的登陆信息来辨别各个人。 在下一节中我们会介绍怎么注册系统并提交作业，现在不需要管。

## 助教会如何测试我的代码？ <a href="#zhu-jiao-hui-ru-he-ce-shi-wo-de-dai-ma" id="zhu-jiao-hui-ru-he-ce-shi-wo-de-dai-ma"></a>

对于助教来说，很难一一审查每个人的代码来验证大家写得正不正确，所以我们会采用测试的方法来给大家评分。像我们发布给同学的doctest一般都写得比较简单，所以那些写得不正确的代码也有可能通过doctest，比如像下面这段代码，本来助教希望大家写`return a + b`，但有个小机灵鬼直接返回`3`试图蒙混过关：

```python
def add(a, b):
    """return the sum of a and b

    >>> add(1, 2)
    3
    """
    return 3
```

但如果我们的测试写得越“详细”，写得不正确的代码就越难蒙混过关。 同学们可以试试下面这段代码能不能通过 doctest。

```python
def add(a, b):
    """return the sum of a and b

    >>> add(1, 2)
    3
    >>> add(3, 4)
    7
    """
    return 3
```

因此，助教们设置了一个在线测评(Online Judge, OJ)网站，用更加“详细”的、对大家隐藏起来的测试来给大家评分，尽可能防止不正确的代码蒙混过关，维护认真做实验的同学的权利。我们会在下一节中教大家如何提交作业，让助教测试你的代码。

好复杂

本节关于测试的介绍，如果大家理解得不清楚也没关系。重点是记住下一节要讲的提交作业的方法，并知道如何查看自己写的代码拿了多少分。
