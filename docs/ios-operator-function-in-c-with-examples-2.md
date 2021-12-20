# ios 操作符()函数在 C++中的使用示例

> 原文:[https://www . geesforgeks . org/IOs-operator-function-in-c-with-examples-2/](https://www.geeksforgeeks.org/ios-operator-function-in-c-with-examples-2/)

C++中 **ios 类**的**运算符()**方法用于设置该流的任何错误标志。这包括故障位或坏位。

**语法:**

```
operator void*() const;

```

**参数:**此方法不接受任何参数。

**返回值:**如果在该流中设置了任何错误位，则该方法返回空指针。

**例 1:**

```
// C++ code to demonstrate
// the working of operator() function

#include <bits/stdc++.h>
using namespace std;

int main()
{

    // Stream
    stringstream ss;

    // Using operator() function
    if (ss) {
        cout << "No error bit is set.\n";
    }
    else {
        cout << "Error bit is set.\n";
    }

    return 0;
}
```

**输出:**

```
No error bit is set.

```

**例 2:**

```
// C++ code to demonstrate
// the working of operator() function

#include <bits/stdc++.h>
using namespace std;

int main()
{

    // Stream
    stringstream ss;
    ss.clear(ss.failbit);

    // Using operator() function
    if (ss) {
        cout << "No error bit is set.\n";
    }
    else {
        cout << "Error bit is set.\n";
    }

    return 0;
}
```

**输出:**

```
Error bit is set.

```

**参考:**T2【hhttp://www . cplusplus . com/Reference/IOs/IOs/operator/