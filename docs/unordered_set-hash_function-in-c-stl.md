# c++ STL 中的无序 _ 集合 hash_function()

> 原文:[https://www . geesforgeks . org/unordered _ set-hash _ function-in-c-STL/](https://www.geeksforgeeks.org/unordered_set-hash_function-in-c-stl/)

**无序 _ 集合::hash_function()** 是 C++ STL 中的一个内置函数，用来获取 hash 函数。这个散列函数是一个一元函数，只接受一个参数，并根据它返回一个 size_t 类型的唯一值。

**语法**:

```cpp
*unordered_set_name*.hash_function()
```

**参数**:函数不接受参数。

**返回值**:函数返回哈希函数。

下面的程序说明了*无序 _ 集合::hash_function()* 函数:

**程序 1** :

```cpp
// CPP program to illustrate the
// unordered_set::hash() function

#include <iostream>
#include <string>
#include <unordered_set>

using namespace std;

int main()
{

    unordered_set<string> sampleSet = { "geeks1", "for", "geeks2" };

    // use of hash_function
    unordered_set<string>::hasher fn = sampleSet.hash_function();

    cout << fn("geeks") << endl;

    for (auto it = sampleSet.begin(); it != sampleSet.end(); it++) {
        cout << *it << " ";
    }
    cout << endl;

    return 0;
}
```

**Output:**

```cpp
15276750567035005396
geeks2 geeks1 for

```

**程序 2** :

```cpp
// CPP program to illustrate the
// unordered_set::hash() function

#include <iostream>
#include <string>
#include <unordered_set>

using namespace std;

int main()
{

    unordered_set<string> sampleSet;

    // use of hash_function
    unordered_set<string>::hasher fn = sampleSet.hash_function();

    cout << fn("geeksforgeeks") << endl;

    return 0;
}
```

**Output:**

```cpp
5146686323530302118

```