# Data Abstraction

Data abstraction is a powerful concept in computer science that allows programmers to treat code as objects -- for example, car objects, chair objects, people objects, etc. That way, programmers don't have to worry about the detail of code/implementation -- we just have to know _what_ it does instead of _how_ it is done.

Data abstraction mimics how we think about the world. When you want to drive a car, you don't need to know how the engine was built or what kind of material the tires are made of. You just have to know how to turn the wheel and press the gas pedal.

In programming languages, an important way to abstraction is to use _abstract data types_. An abstract data type (ADT for short) consists of two types of functions:

* **Constructors**: functions that create the abstract data using existing information.
* **Selectors**: functions that retrieve information from the abstract data.

Programmers design ADTs to abstract away how information is stored and calculated such that the users of these data types do _not_ need to know how constructors and selectors are implemented. The nature of _abstract_ data types allows users to assume that the functions have been written correctly and work as described, and they just have to use them (without worrying the details).
