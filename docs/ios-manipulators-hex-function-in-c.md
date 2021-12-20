# ios 操纵器 hex()在 C++中的功能

> 原文:[https://www . geesforgeks . org/IOs-机械手-hex-function-in-c/](https://www.geeksforgeeks.org/ios-manipulators-hex-function-in-c/)

C++中**流操纵器**的 **hex()** 方法用于设置指定字符串流的基线格式标志。该标志设置十六进制数的基线。因此，输出以十六进制为基数显示数字。

**语法:**

```cpp
ios_base& hex (ios_base& str)

```

**参数:**该方法接受**字符串**作为参数，该参数是受格式标志影响的流。

**返回值:**该方法返回设置了内部格式标志的**流**字符串。

**例 1:**

```cpp
// C++ code to demonstrate
// the working of hex() function

#include <iostream>

using namespace std;

int main()
{

    // Initializing the number
    int n = 321;

    // Using hex()
    cout << "hex flag: "
         << hex << n << endl;

    return 0;
}
```

**输出:**

```cpp
hex flag: 141

```

**例 2:**

```cpp
// C++ code to demonstrate
// the working of hex() function

#include <iostream>

using namespace std;

int main()
{

    // Initializing the number
    int n = -321;

    // Using hex()
    cout << "hex flag: "
         << hex << n << endl;

    return 0;
}
```

**输出:**

```cpp
hex flag: fffffebf

```

**参考:**T2】http://www.cplusplus.com/reference/ios/hex/