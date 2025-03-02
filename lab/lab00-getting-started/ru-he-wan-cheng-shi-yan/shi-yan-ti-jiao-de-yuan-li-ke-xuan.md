# 实验提交的原理（可选）

下载插件，点点鼠标运行，敲敲键盘写作业，再点点鼠标提交，编程真的 so easy！ 你有没有想过这一切背后的原理是什么？

> 本章为可选内容。
>
> 在进行后面的内容之前，请准备好终端。 未经特殊说明的操作在 Windows/macOS/Linux 效果都是类似的。

## 打开终端 <a href="#da-kai-zhong-duan" id="da-kai-zhong-duan"></a>

对于使用 Windows 的同学，请在开始菜单中搜索 "powershell" 并打开。

一般来说，终端里运行的是一个特殊的 _shell_ 程序。 如果你用的是 Windows，那么会是 powershell；如果你用的是 macOS，那么就是 zsh；如果你用的是 Linux，那么大概率会是 bash。

## 终端漫游 <a href="#zhong-duan-man-you" id="zhong-duan-man-you"></a>

打开终端后，shell 会展示一&#x4E2A;_&#x5DE5;作目录_（Working Directory），它表明你现在正处在哪个文件夹下。

每个人在刚进入终端时的工作目录可能都有所不同，Windows 可能会在最前面加上文件夹所在&#x7684;_&#x76D8;符_（就是大家熟知的C盘、D盘等等）。 为了方便起见，后面我们会省略与讲解内容无关的文件夹前缀和盘符（或者用户名，如果你用的是 macOS 或者 Linux）。

以助教的 shell 为例，助教此时正处在 `homework` 文件夹中：

```bash
~/homework$ 
```

为了查看 `homework` 文件夹里都有什么东西，你可以输入命令 `ls`[1](https://sicp.pascal-lab.net/2024/labs/lab00/4_5.html#1) 后按回车：

```bash
~/homework$ ls
lab00-Code lab01-Code
~/homework$ 
```

如果一切顺利，你将会看到工作目录下的所有文件。 例如助教就在 `homework` 目录里放置了下载并解压完毕的 `lab00-Code` 文件夹和 `lab01-Code` 文件夹。

### 进入一个文件夹 <a href="#jin-ru-yi-ge-wen-jian-jia" id="jin-ru-yi-ge-wen-jian-jia"></a>

当然工作目录并不总是处在我们希望的位置，能不能像串门一样换一个工作目录呢？

答案是可以的。 在终端输入 `cd lab00-Code`[2](https://sicp.pascal-lab.net/2024/labs/lab00/4_5.html#2) 后回车，就会发现工作目录现在变成了 `lab00-Code` 这个文件夹。再执行 `ls` 指令就会发现我们下载好的文件都在里面了。

```bash
~/homework$ cd lab0-Code
~/homework/lab00-Code$ ls
hello.py  lab00.ok  lab00.py  ok
```

> 输出的格式不一定完全相同，但应当至少包含 `ok`、`lab00.py`、`hello.py`和`lab00.ok` 四个文件。

同名的文件夹可能有很多（例如程序设计课也可能会有 `lab00-Code`），为了表示 `homework` 下面的这个 `lab00-Code`，我们会用 `homework/lab00-Code` 这样以 `/` 连接&#x7684;_&#x6587;件路径_（File Path）称呼它，以区别于其他文件夹下的 `lab00-Code`。

### 退出当前文件夹 <a href="#tui-chu-dang-qian-wen-jian-jia" id="tui-chu-dang-qian-wen-jian-jia"></a>

除了进入一个文件夹，还可以退出一个文件夹。 例如现在我们想要退出 `lab00-Code` 文件夹，回到 `homework` 文件夹，然后去看看别的作业。那么我们可以输入 `cd ..`

```bash
~/homework/lab00-Code$ cd ..
~/homework$ ls
lab00-Code lab01-Code
```

可以看到，我们 `ls` 的结果又变成了一开始的样子，这说明现在的工作目录又回到了 `homework` 这个文件夹。

### 切换盘符（Windows） <a href="#qie-huan-pan-fu-windows" id="qie-huan-pan-fu-windows"></a>

以从 C 盘切换到 D 盘为例。在终端中输入 `D:` 后回车：

```powershell
PS C:\> D:
PS D:\> 
```

## 提交作业 <a href="#ti-jiao-zuo-ye" id="ti-jiao-zuo-ye"></a>

> 现在，请你利用刚刚掌握的命令，把工作目录切换到 `lab00-Code` 这个解压后的实验文件夹下。

前面提到我们用 ok 来提交实验。 在使用 `ls` 命令时，你应该看到了两个和 ok 相关的文件，分别是 `ok` 和 `lab00.ok`。

### lab00.ok <a href="#lab00ok" id="lab00ok"></a>

你可以用编辑器打开 `lab00.ok` 看看里面的内容。 `lab00.ok` 描述了：

1. 实验的名字，这里是 `Getting Started`
2. 需要提交程序的名字，这里是 `lab00.py`
3. 测试，这里 ok 给每个实验都安排了 doctest 测试
4. 和一些你暂时不知道也没有关系的内容

```json
{
    "name": "Getting Started",
    "endpoint": "lab00",
    "src": [
        "lab00.py"
    ],
    "tests": {
        "lab00.py:twenty_twenty_four": "doctest",
        "lab00.py:sum": "doctest",
        "lab00.py:diff_square": "doctest"
    },
    "protocols": [
        "file_contents",
        "grading",
        "unlock",
        "analytics",
        "backup"
    ]
}
```

`lab00.ok` 是指导 `ok` 怎么**本地测试**和提交我们的程序&#x7684;_&#x914D;置文件_（Configuration File），它就像助教写给 `ok` 的任务。

## 用 ok 提交作业 <a href="#yong-ok-ti-jiao-zuo-ye" id="yong-ok-ti-jiao-zuo-ye"></a>

`ok` 是负责提交实验的程序。

要本地测试某一道具体的题目（例如`twenty_twenty_four`）只需要输入

```bash
python ok -q twenty_twenty_four --local
```

要本地测试所有题目只需要输入

```bash
python ok --local
```

要提交所有题目只需要输入

```bash
python ok --submit
```

> 这么多用法，助教是怎么知道要这么用的？

这是个很好的问题！ 实际上助教也不是生来就知道怎么用 `ok` 的。

要想知道 `ok` 的用法，只需要在终端里输入 `python ok --help`，精简后的输出内容展示如下：

```bash
$ python ok --help
usage: python ok [--help] [options]
...
You can run all tests with

    python ok
...
```

这里 `--help` 的用途是让 `ok` 告诉我们怎么让它替我们交作业（或者是做一些别的事情）。 这段文字虽然长，但理解起来并不困难，你可以试着扫一眼看看能不能发现什么有趣的事情。

## 插件的原理 <a href="#cha-jian-de-yuan-li" id="cha-jian-de-yuan-li"></a>

TBD

1&#x20;

ls 的全称是 List

2&#x20;

cd 的全称是 Change Directory
