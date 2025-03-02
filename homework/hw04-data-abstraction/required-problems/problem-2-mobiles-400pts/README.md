# Problem 2: Mobiles (400pts)

> _Acknowledgements_:
>
> This mobile example is based on a classic problem from Structure and Interpretation of Computer Programs, [Section 2.2.2](https://web.mit.edu/6.001/6.037/sicp.pdf).

![](https://sicp.pascal-lab.net/2024/homework/hw04/images/mobile-planet.png)

We are making a planetarium mobile. A [mobile](https://en.wikipedia.org/wiki/Mobile_\(sculpture\)) is a type of hanging sculpture. A binary mobile consists of two arms. Each arm is a rod of a certain length, from which hangs either a planet or another mobile.

![](https://sicp.pascal-lab.net/2024/homework/hw04/images/mobile-planet-labeled.png)

We will represent a binary mobile using the **data abstractions** below:

* A mobile has a left arm and a right arm.
* An arm has a positive length and something hanging at the end, either a mobile or planet.
* A planet has a positive size.
