# 表达式与语句

接下来，我们来正式学习一下表达式和语句的概念，并在 Python 解释器的交互模式中来检查它们的执行结果。

大家在高中阶段一定见过`8 * 8`, `a + b` , `7 - (x + y)`之类的数学表达式， 而程序表达式也是类似的，它们由数字（亦称为常数）、变量(如`a`, `x`等，用字母表示)、运算符（如加法、乘法符号等）等组成， 一些表达式还包含了函数，这在课上会讲到（不妨试着用数学里的“函数”概念去理解它）。 我们知道，如果表达式里面每个部分的值都是已知的（例如，`a + b`中`a`的值为`4`、`b`的值为`5`），那么整个表达式就可以被求值。 让我们来看看Python里面的表达式和求值是什么样的。

## 基本表达式 <a href="#id-1-ji-ben-biao-da-shi" id="id-1-ji-ben-biao-da-shi"></a>

基本表达式（Primitive Expressions）只需要一步便可以求得它的值，例如整数、_浮点数_（Floating point numbers）&#x548C;_&#x5E03;尔_（Boolean）值：

```python
>>> 3
3
>>> 12.5
12.5
>>> True
True
```

操作

在交互模式下输入你能想到的基本表达式，并按回车键查看结果。

浮点数？

浮点数是一种带小数点的数。之所以叫它浮点数，是因为它有着可以浮动的小数点。浮点数的具体细节与数字在计算机中的底层表示有关，大家在《计算机系统基础》这门课上会进行深入学习（和考试），现在了解即可。

变量名同样也是基本表达式，求值的结果为在当前程序的状态下绑定到的值。我们把与变量相关的内容留在[赋值语句的部分](https://sicp.pascal-lab.net/2024/labs/lab00/3_2.html#4-%E8%B5%8B%E5%80%BC%E8%AF%AD%E5%8F%A5)。

## 布尔值与布尔表达式 <a href="#id-2-bu-er-zhi-yu-bu-er-biao-da-shi" id="id-2-bu-er-zhi-yu-bu-er-biao-da-shi"></a>

布尔值只有两种值，`True`和`False`，表示逻辑上的“真”与“假”。

例如，我们知道数字1是不等于2的，所以若在Python交互模式中输入`1 == 2`（这个表达式意思是“1等于2”，在 Python 中一般用`==`表示“相等”）， 则会得到它的值为`False`；相反，如果输入`1 != 2`（表示”1不等于2“，在Python中一般用`!=`表示”不相等“），则会得到值`True`。

这种能计算出布尔值的表达式我们称之&#x4E3A;_&#x5E03;尔表达式_（Boolean Expression）。

```python
>>> 1 == 2
False
>>> 2 == 1
False
>>> 1 != 2
True
```

操作

在交互模式下输入你能想到的布尔表达式，并按回车键查看结果。

## 算术表达式 <a href="#id-3-suan-shu-biao-da-shi" id="id-3-suan-shu-biao-da-shi"></a>

可以通过对数字和数学运算符的组合产生复杂&#x7684;_&#x7B97;术表达式_（Arithmetic Expression）。 Python 中常见的数学运算有`+`(加)、`-`(减)、`*`(乘)、`**`(乘方)和以下三种：

* 浮点除法 (`/`)：计算第一个数除以第二个数的结果，得到一个浮点数（即使能够整除）。
* 下取整除法 (`//`)：计算第一个数除以第二个数的下取整后的结果，得到一个整数。
* 取模 (`%`)：计算第一个数除以第二个数的余数(>0), 得到一个整数。

```python
>>> 1 + 2
3
>>> 3 - 2
1
>>> 5 * 6
30
>>> 7 / 4
1.75
>>> 7 // 4
1
>>> 7 % 4
3
>>> 4 ** 3
64
>>> 2 / 0
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
ZeroDivisionError: division by zero
```

除以0？

```python
>>> 1 / 0
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
ZeroDivisionError: division by zero
```

Python 并没有给出任何结果，而是返回了一&#x4E2A;_&#x9519;误_（Error）。 这是因为对 `0` 作除法没有意义，Python 觉得这是一个错误。

像大家平时学过的数学运算一样，算数操作也有优先级，比如乘方运算的优先级大于乘除运算，乘除运算的优先级大于加减运算。 同样地，你也可以通过“加括号”来改变求值优先级。注意，优先级不需要记忆。当你对运算优先级拿不准的时候，就多加括号！

```python
>>> 2 + 6 / 4
3.5
>>> (2 + 6) / 4
2.0
```

操作

在交互模式下输入你能想到的算术表达式，并按回车键查看结果。

## 赋值语句 <a href="#id-4-fu-zhi-yu-ju" id="id-4-fu-zhi-yu-ju"></a>

一&#x4E2A;_&#x8D4B;值语句_（Assignment Statement）由一个变量名和一个表达式组成。它会把变量名与该表达式的值绑定。

```python
>>> a = (100 + 50) // 2
```

> 注意：在Python中，不能对语句进行求值。

```python
>>> None==(a=1)
  File "<stdin>", line 1
    None==(a=1)
            ^
SyntaxError: invalid syntax
```

你可以输入一个之前定义过的变量名，例如a，Python 解释器会输出其绑定到的值。如果你还记得之前的内容，`a`也是一个基本表达式：

```python
>>> a
75
```

注意这里`a`被绑定到`75`, 而非`(100 + 50) // 2` —— 变量名绑定到值而非表达式上。

## print <a href="#id-5-print" id="id-5-print"></a>

`print()`是Python的内置函数，它可以将一个表达式的值输出到终端上（如果还不清楚函数的概念，就单纯记忆一下它的用法吧）。 `print(2024)`也是一条语句：

```python
>>> 2024
2024
>>> print(2024)
2024
>>> 2023 + 1
2024
>>> print(2023 + 1)
2024
```

特殊的`print`

上面在**交互模式**下输入`2024`和`print(2024)`显示的结果看上去相同，但前者是交互模式下自动输出的每一行表达式的值， 后者是`print()`在终端中的输出。在**非交互模式**下（即执行Python代码时，[后面](https://sicp.pascal-lab.net/2024/labs/lab00/3_4.html)会讲），如果你想知道结果，请用`print()`。