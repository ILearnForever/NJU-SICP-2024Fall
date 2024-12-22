# Python解释器

刚才我们说过，Python 解释器是用来执行 Python 代码的软件。 Python 的交互模式能够让我们一边输入代码，一边查看代码的执行结果——这样可以快速尝试，得到反馈，是很好的学习 Python 的做法。 我们来看看如何启动 Python 解释器的“交互模式”。

## VSCode 终端（推荐） <a href="#vscode-zhong-duan-tui-jian" id="vscode-zhong-duan-tui-jian"></a>

操作

打开 VSCode 终端后，向其中输入 `python`，按下回车。

## IDLE <a href="#idle" id="idle"></a>

[_IDLE_](https://docs.python.org/3/library/idle.html)（Integrated Development and Learning Environment）是 Python 自带的交互环境。

注意

IDLE不是终端

操作

以 Windows 为例，在安装好 Python 后，我们在开始菜单中搜索 `IDLE` 以启动交互模式。

## 认识交互界面 <a href="#ren-shi-jiao-hu-jie-mian" id="ren-shi-jiao-hu-jie-mian"></a>

如果一切顺利，你会发现屏幕上出现了这样一串文字（可能有出入）：

```shell
Python 3.10.7 (tags/v3.10.7:6cc6b13, Sep  5 2023, 14:08:36) [MSC v.1933 64 bit (AMD64)] on win32
Type "help", "copyright", "credits" or "license" for more information.
>>>
```

大家很可能看不懂这串东西。不过不用慌，我们带大家分析一下上面的几行文字。首先是前两行：

```shell
Python 3.10.7 (tags/v3.10.7:6cc6b13, Sep  5 2023, 14:08:36) [MSC v.1933 64 bit (AMD64)] on win32
Type "help", "copyright", "credits" or "license" for more information.
```

这是Python解释器开始运行交互模式后打印的一些信息，比如第一行打头的“Python 3.10.7”这个版本号。 接着，Python 说我们可&#x4EE5;_&#x8F93;入_（Type）"`help`"、"`copyright`"、"`credits`"或者"`license`" 来获取更多信息。 我们不必在意。大家显示的信息不必和这里展示的信息完全一致，但版本号必须是3.x.y的形式。

接着，Python 显示了 `>>>` 这&#x4E2A;_&#x63D0;示符_（Prompt）。 这个符号就像是数学题目后的“解：”，它表示 Python 正在等待着你的输入。 我们现在不妨给 Python 出一道数学题，看看 Python 会不会计算小学生都会算的事情。

操作

在提示符 `>>>` 后输入 `1 + 1`，按下回车键。

结果如下：

```python
>>> 1 + 1
2
```

可以看到，Python 很灵性地计算了 `1 + 1`，得到 `2`，并把 `2` 输出给你看，然后很积极地再打出了提示符 `>>>`，提醒你输入下一个表达式或语句来让它计算。

概言之，交互模式便是一种“你输入表达式或语句，Python 解释器执行它，Python 把结果告诉你，你再输入表达式或语句，Python解释器再执行它……”的重复过程， 直到你不想再和 Python 解释器说话，敲入 `exit()` 或者 `quit()` 后按下回车，交互模式就结束了。

注意

代码块中展示的 `>>>` 并不是 Python 程序的一部分，不需要复制到交互模式中。
