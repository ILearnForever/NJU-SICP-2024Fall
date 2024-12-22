# 提交作业与评分

为了获取分数，我们需要使用随作业下发的 Ok 客户端进行测试并提交。 这里助教特别强调，所有作业都必须使用 Ok 进行测试并提交，作业系统不再提供直接上传文件的提交功能。

为什么要用Ok?

**使用Ok（VSCode的SICP插件）是保护作业文件、遵守学术诚信的有效手段**。 UC Berkeley开发的Ok是一个对作业进行测试、备份、提交的程序。 助教在2021年的时候把Ok进行了魔改，支持了我们自己的作业系统。 张天昀助教在2022年开发了VSCode插件，使得使用Ok不再需要使用终端。 以上所有工具目前都由我们（现任助教）维护，如果发现问题/有建议欢迎向我们提出。

**Ok会把你的程序备份到作业系统**。 如果你一不小心手滑把电脑砸了/掰成两半了/泡水里了[1](https://sicp.pascal-lab.net/2024/labs/lab00/4_4.html#1)/格式化了，可以向助教索要最新的备份文件，当然最好的方法就是自己保存好代码。 同时，大家完成作业产生的一系列备份文件，可以用于调查是否存在违反学术诚信的行为，也可以帮助自己证明自己是独立完成作业的。 从2021年至今收集到的数据来看，很多同学完成困难的作业题需要尝试十几次才能获得满分。

我们考虑这样的一个例子：同学A的在布置作业后一直没有任何尝试，在截止日期当晚直接满分，助教都认为困难的题目没有任何尝试就做对了，且复杂的代码与同学B的高度相似。 在没有能够证明A自己独立完成作业的可信证据的情况下，其行为将被认定为抄袭。 作业抄袭或其他学术不端行为初犯将取消作业成绩（两人的成绩都为0），再犯则课程成绩按0分计并提交到本科生院。

[1](https://sicp.pascal-lab.net/2024/labs/lab00/4_4.html#1)：真实的事件，某位2019级拔尖班学长喝饮料的时候把饮料浇到了电脑上。

## 系统注册 <a href="#xi-tong-zhu-ce" id="xi-tong-zhu-ce"></a>

操作

1. 在[南京大学电子邮件系统](https://mail.smail.nju.edu.cn/)开通自己的学生邮箱，如何开通请看[【IT服务】南大邮箱系列问答](https://itsc.nju.edu.cn/1b/ce/c21586a334798/page.htm)。
2. 在[南京大学代码托管系统](https://git.nju.edu.cn/)使用自己的学生邮箱注册一个账号。
   * 第一次登录本课程作业系统**必须使用学号邮箱**，不能是自定义的邮箱地址。
   * 如果你已经用其他邮箱注册过代码托管系统，可以在用户设置页面修改自己的邮箱。
3. 点击填写[SICP2024作业系统注册&小调查](https://table.nju.edu.cn/dtable/forms/custom/sicp2024-register/)，填写完成后过几秒钟就可以登录作业系统了。

好麻烦

你可能会问，为什么不用用户名密码登录的方式？

1. 管理密码需要成本，~~助教很懒~~。
2. 很多同学一直都用默认密码[2](https://sicp.pascal-lab.net/2024/labs/lab00/4_4.html#2)。
3. 代码托管系统提供了重置密码、两步验证等功能，更安全。

[2](https://sicp.pascal-lab.net/2024/labs/lab00/4_4.html#2)：真实的事件，弱密码可能会被别人登录账户以下载作业。

## 提交作业 <a href="#ti-jiao-zuo-ye" id="ti-jiao-zuo-ye"></a>

打开实验中的代码文件，在VSCode中,按下`Ctrl+Shift+P`（在macOS里是`Command+Shift+P`）打开`Command Palette`（中文应该是`命令面板`），然后输入submit来进行搜索，点击`Submit your code`即可提交。

![](https://sicp.pascal-lab.net/2024/labs/lab00/images/vsc-sicp-submit.png)

如果你不习惯使用键盘快捷键，也可以点击VSCode左下角的齿轮，然后点击`命令面板`，即可打开命令面板。

![](https://sicp.pascal-lab.net/2024/labs/lab00/images/vsc-command-palette.png)

操作

根据指引提交你的作业。

运行`Submit your code`后，VSCode底部会弹出终端。如果提交成功，Ok会打印提交ID，并展示你提交的得分。

```bash
=====================================================================
Assignment: lab00 Getting Started
OK, version XXXX.X.XX
=====================================================================

Submitting lab00 by TA 助教A.
Online Judge received submission ID XXXXXXXX
Open in browser: https://sicp.pascal-lab.net/oj

Waiting for online judge to grade, press Ctrl+C to exit

... 5s
---------------------------------------------------------------------
Submission graded: score = 33% (100 / 300)
 -> P1: 100
 -> P2: 0
 -> P3: 0
Updating OK: XXXX.XX.XX
Updated to version: XXXX.XX.XX
```

## 查看评分 <a href="#cha-kan-ping-fen" id="cha-kan-ping-fen"></a>

打开课程主页，点击右上角的“Online Judge”进入作业系统并登录。

![](https://sicp.pascal-lab.net/2024/labs/lab00/images/online_judge_homepage.png)

在左边选择“作业列表”，右边就会展示你已经提交的所有作业的得分（多次提交只计算最高得分），该OJ目前只能用来查看分数和截止时间。（其他功能正在开发中qwq）

分数计算规则

每次作业的最终得分为你所有提交中的最高得分。

![](https://sicp.pascal-lab.net/2024/labs/lab00/images/online_judge_assignment.png)

## 常见问题 <a href="#chang-jian-wen-ti" id="chang-jian-wen-ti"></a>

**Q: 作业可以提交多少次？**

A: 未经特殊说明的题目，在截止时间之前（以服务器时间为准）你可以提交任意多的次数。 提交的次数不会影响你的成绩。

**Q: 我把电脑借给别人了。别人不小心用我的账号提交了他的代码怎么办？**

A: 请马上联系助教说明情况，越早越好，避免误会。

**Q: 我来不及完成作业了，怎么办？**

A: 原则上不允许作业迟交，没有提交的作业均为0分。如果遇到特殊/紧急情况，请马上与助教联系，视情况给予补交机会。
