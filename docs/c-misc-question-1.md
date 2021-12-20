# C | Misc |问题 1

> 原文:[https://www.geeksforgeeks.org/c-misc-question-1/](https://www.geeksforgeeks.org/c-misc-question-1/)

用 C 语言

**(A)** 当前激活记录与主
的激活记录之间最多存在一条激活记录 **(B)** 当前激活记录与主的激活记录之间的激活记录数量取决于实际的函数调用顺序。
**(C)** 全局变量的可见性取决于实际的函数调用顺序。
**(D)** 递归需要将递归函数的激活记录保存在不同的堆栈上，然后才能调用递归函数。

**回答:****(B)**

**解释:**a)–>C 语言中没有这样的限制
B)–>True
C)–>False。在 C 语言中，变量是静态范围的，而不是动态范围的。
c)–>假。激活记录存储在同一个堆栈中。