# C

中的 moverel()函数

> 原文:[https://www.geeksforgeeks.org/moverel-function-c/](https://www.geeksforgeeks.org/moverel-function-c/)

头文件 graphics.h 包含 **moverel()** 函数，该函数将一个点从当前位置(x_pos1，y_pos1)移动到与当前位置有相对距离(x，y)的点，然后将当前位置向前移动(x，y)。
**注:** **getx** 和 **gety** 可用于查找当前位置。

**语法:**

```
moverel(int x, int y);

The end position is calculated as :
x_pos2 = x_pos1 + x;
y_pos2 = y_pos1 + y;

```

**示例:**

```
Input : x_pos1 = 0, y_pos1 =0, x = 200, y = 100
Output : 

Input : x_pos1 = 100, y_pos1 = 150, x = 150, y = 60
Output : 

```

**情况 1 :** 当前位置在原点时，即(0，0)

下面是 C 语言中 moverel()函数的实现:

```
// C Implementation for moverel()
#include <graphics.h>
#include<stdio.h>

// driver code
int main()
{
    // gm is Graphics mode which is
    // a computer display mode that
    // generates image using pixels.
    // DETECT is a macro defined in
    // "graphics.h" header file
    int gd = DETECT, gm;
    char arr[100];

    // initgraph initializes the
    // graphics system by loading a
    // graphics driver from disk
    initgraph(&gd, &gm, "");

    // moverel function
    moverel(200, 100);

    // sprintf stands for “String print”.
    // Instead of printing on console,
    // it store output on char buffer
    // which are specified in sprintf
    sprintf(arr, "Current x position = %d and "
             "y position = %d",getx(), gety());

    // outtext function displays
    // text at current position.
    outtextxy(100, 150, arr);

    getch();

    // closegraph function closes the
    // graphics mode and deallocates
    // all memory allocated by
    // graphics system .
    closegraph();

    return 0;
}
```

输出:

**情况 2 :** 当前位置不是原点(100，150)时。

下面是 C 语言中 moverel()函数的实现:

```
// C Implementation for moverel()
#include <graphics.h>
#include<stdio.h>

// driver code
int main()
{
    // gm is Graphics mode which is
    // a computer display mode that
    // generates image using pixels.
    // DETECT is a macro defined in
    // "graphics.h" header file
    int gd = DETECT, gm;
    char arr[100];

    // initgraph initializes the
    // graphics system by loading a
    // graphics driver from disk
    initgraph(&gd, &gm, "");

    // moveto function to change
    // initial position
    moveto(100, 150);

    // moverel function
    moverel(150, 60);

    // sprintf stands for “String print”.
    // Instead of printing on console,
    // it store output on char buffer
    // which are specified in sprintf
    sprintf(arr, "Current x position = %d and "
             "y position = %d",getx(), gety());

    // outtext function displays
    // text at current position.
    outtextxy(100, 150, arr);

    getch();

    // closegraph function closes the
    // graphics mode and deallocates
    // all memory allocated by
    // graphics system .
    closegraph();

    return 0;
}
```

输出: