# 执行Python文件

大家已经知道，Python代码是由表达式和语句组成的。而现在大家已经学会了一些简单的表达式和语句，并在交互模式下体验了执行它们的效果。 现在，我们就可以把之前学过的表达式和语句都写入到文件中，然后让Python解释器直接从文件中读取它们并执行。

关于编写代码，我们已经事先准备了一个编写好的文件`hello.py`（约定俗成，大家以`.py`的后缀来表示这是一个Python代码文件）。 这个文件中有下面内容：

```python
2024
print(2024)
```

## 在 VSCode 中执行（推荐） <a href="#zai-vscode-zhong-zhi-xing-tui-jian" id="zai-vscode-zhong-zhi-xing-tui-jian"></a>

操作

在 VSCode 中打开下发的实验文件夹。

### VSCode 终端派 <a href="#vscode-zhong-duan-pai" id="vscode-zhong-duan-pai"></a>

操作

打开 VSCode 的终端，然后在里面输入命令

```bash
python hello.py
```

然后就可以在 VSCode 的终端里看到程序的结果:

```bash
2024
```

### VSCode 鼠标派 <a href="#vscode-shu-biao-pai" id="vscode-shu-biao-pai"></a>

如果你的VSCode安装了python插件，那你就可以在右上角看到一个三角形的图标。

操作

点击右上角的绿色三角形以运行打开的 Python 文件。

![](https://sicp.pascal-lab.net/2024/labs/lab00/images/vscode_run.png)

然后就可以在 VSCode 的终端里看到程序的结果:

```bash
2024
```

## 脚本模式 <a href="#jiao-ben-mo-shi" id="jiao-ben-mo-shi"></a>

这种一次性执行文件中的全部代码，然后结束运行的 Python 工作模式，就是脚本模式。

你也可以利用任何任何文本编辑器修改`hello.py`，尝试前面提到的其它表达式和语句，或者试一试其它你感兴趣的内容。

到底有几个`2024`？

程序里明明有两个 `2024`，为什么终端里只显示了一个 `2024`？

可以回顾一下[前面的内容](https://sicp.pascal-lab.net/2024/labs/lab00/3_2.html#5-print)。 你会发现，原来`2024`这种表达式仅会在交互模式下显示求值结果。这里不是交互模式，所以表达式`2024`没有显示任何结果。 屏幕上的`2024`是由print函数“打印”出来的（难怪它叫`print`）！
