# c++ 中的 ratio_equal()示例

> 原文:[https://www . geesforgeks . org/ratio _ equal-in-c-with-examples/](https://www.geeksforgeeks.org/ratio_equal-in-c-with-examples/)

**ratio_equal()** 是 C++ STL 中的一个内置函数，用于检查两个给定的比率是否相等。

**语法:**

```cpp
template < class ratio1_name, class ratio2_name > ratio_equal

```

**模板参数:**该功能接受两个要比较的模板参数*比率 1* 和*比率 2* 。

**返回值:**如果比率相等，函数返回真，否则返回假。

下面的程序说明了 ratio_equal()函数:

**程序 1:**

```cpp
// C++ program to illustrate the
// ratio_equal function
#include <iostream>
#include <ratio>
using namespace std;
int main()
{
    typedef ratio<3, 9> ratio1;
    typedef ratio<1, 3> ratio2;

    // If both the ratios are same
    if (ratio_equal<ratio1, ratio2>::value)
        cout << "Both ratio are equal";
    else
        cout << "Both ratio are not equal";

    return 0;
}
```

**Output:**

```cpp
Both ratio are equal

```

**程序 2:**

```cpp
// C++ program to illustrate the
// ratio_equal function
#include <iostream>
#include <ratio>
using namespace std;
int main()
{
    typedef ratio<1, 2> ratio1;
    typedef ratio<5, 4> ratio2;

    // If both the ratios are same
    if (ratio_equal<ratio1, ratio2>::value)
        cout << "Both ratio are equal";
    else
        cout << "Both ratio are not equal";

    return 0;
}
```

**Output:**

```cpp
Both ratio are not equal

```