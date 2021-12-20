# 如何使用迭代器

从列表中删除一系列值

> 原文:[https://www . geeksforgeeks . org/如何使用迭代器从列表中删除值范围/](https://www.geeksforgeeks.org/how-to-delete-a-range-of-values-from-the-list-using-iterator/)

给定一个[列表](https://www.geeksforgeeks.org/list-cpp-stl/)，任务是使用迭代器从该列表中删除一系列值。

**示例:**

```cpp
Input: list = [10 20 30 40 50 60 70 80 90],
       start_iterator = 3,
       end_iterator = 8
Output: 10 20 80 90

Input: list = [1 2 3 4 5]
       start_iterator = 1,
       end_iterator = 3
Output: 3 4 5

```

**方法:**在该方法中，从列表中删除一系列元素。这在两个[迭代器](https://www.geeksforgeeks.org/iterators-c-stl/)的帮助下完成。第一个迭代器指向范围的开始元素，第二个迭代器指向范围的最后一个元素。第一个迭代器是*独占*，而最后一个迭代器是*包含*，这意味着最后一个迭代器指向的元素也会被删除。

**语法:**

```cpp
iterator erase (const_iterator startPositionIterator_exclusive, 
                const_iterator endingPositionIterator_inclusive);

```

下面是上述方法的实现:

**程序:**

```cpp
// C++ program to delete an element
// of a List by passing its value

#include <iostream>
#include <list>
using namespace std;

// Function to print the list
void printList(list<int> mylist)
{
    // Get the iterator
    list<int>::iterator it;

    // printing all the elements of the list
    for (it = mylist.begin(); it != mylist.end(); ++it)
        cout << ' ' << *it;
    cout << '\n';
}

// Function to delete the element of list
void deleteRange(list<int> mylist)
{
    // Printing all the elements of the list
    cout << "\nList originally: ";
    printList(mylist);

    // Get the starting Iterator at 3rd element
    list<int>::iterator start_itr = mylist.begin();
    start_itr++;
    start_itr++;

    // Get the ending Iterator at 2nd last element
    list<int>::iterator end_itr = mylist.end();
    end_itr--;
    end_itr--;

    // Erase the elements in the range
    // of the iterators passed as the parameter
    mylist.erase(start_itr, end_itr);

    // Printing all the elements of the list
    cout << "List after deletion of range"
         << " from 3rd till 2nd last: ";
    printList(mylist);
}

// Driver Code
int main()
{
    list<int> mylist;

    // Get the list
    for (int i = 1; i < 10; i++)
        mylist.push_back(i * 10);

    // Delete an element from the List
    deleteRange(mylist);

    return 0;
}
```

**Output:**

```cpp
List originally:  10 20 30 40 50 60 70 80 90
List after deletion of range from 3rd till 2nd last:  10 20 80 90

```