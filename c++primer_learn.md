## 开始C++
主要内容：
- [1.C++ base](#1c-base)
  - [1.1 文件拓展名（cpp）](#11-文件拓展名cpp)
  - [1.2 程序清单](#12-程序清单)
  - [1.3 输入与输出](#13-输入与输出)
    - [1.3.1 名称空间](#131-名称空间)
    - [1.3.2 C++输出（cout）](#132-c输出cout)
    - [1.3.3 输入（cin）](#133-输入cin)
  - [1.4C++源代码的格式化](#14c源代码的格式化)
    - [1.4.1 标记（token）和空白（white space）](#141-标记token和空白white-space)
    - [1.4.2 源代码风格](#142-源代码风格)
  - [2 类](#2-类)
  - [3 函数](#3-函数)
    - [3.1 函数分类](#31-函数分类)
    - [3.2 自定义函数](#32-自定义函数)
      - [3.2.1 函数格式](#321-函数格式)
  


# 1.C++ base

## 1.1 文件拓展名（cpp）

## 1.2 程序清单
```C++
#include <iostream> //a preprocessor directive
int main()          //function header
{                   //start of function body
    using namespace std; //make definitions visible
    cout << "1,2,3,ive"; //message
    cout << endl;       //start a new line    
    return 0;           //terminate main()
}                       //end of function body
```
- 在一些老式编译器上，其中`#include <iostream>`+`using namespace std`可以替换成`#include <iostream.h>`
- `cout << endl`效果等同于`cout << "xxx\n" `
- C++允许在程序的任何地方声明新变量。



## 1.3 输入与输出

### 1.3.1 名称空间

当使用`iostream`时应使用名称空间编译指令`using namespace std`来使`iostream`中的定义对程序可用。

>名称空间让产商将产品封装在一个叫做**名称空间**的单元中，这样可以用名称空间的名称来指出想使用哪个产商的产品，避免重名函数造成的错误。


比如两个封装好的产品都含有`kirsh()`函数，使用名称空间将其分为`enchae version`和`wonyong version`

```C++
enchae::kirsh() //ues enchae namespace version
wonyong::kirsh() //ues wonyong namespace version
```
按照这种方式，在使用`iostream`时省略`using namespace std`的写法：
```C++
std::cout <<"1,2,3,ive";
std::cout << std::endl;
```
----

### 1.3.2 C++输出（cout）

```C++
cout <<"movie star";
```

>cout的对象属性包括一个插入操作符（<<），它将其右侧的信息插入到输出流中。

```C++
cout <<"movie star?" <<idkh <<"daydream" <<endl;
```

效果等同：
```C++
cout <<"movie star?"； 
cout <<idkh ;
cout <<"daydream" ;
cout <<endl;
```

或者
```C++
cout <<"movie star?"； 
     <<idkh ;
     <<"daydream" ;
     <<endl;
```

运行结果（`idkh`需进行定义，这里定义的是`int idkh`）
`movie star?0daydream`


----

### 1.3.3 输入（cin）

```C++
cin >> xore
```

信息从`cin`流向`xore`，即`cin`使用操作符>>从输入流中抽取字符。


---
---


## 1.4C++源代码的格式化
### 1.4.1 标记（token）和空白（white space）

```C++
return 0; //INVALID 
return (0); //VALID,white space omitted
```

---

### 1.4.2 源代码风格
- 每行一条语句
- 每个函数都有一个开始和结束花括号，各占一行。
- 函数中语句相对于花括号缩进。
- 与函数名称相关的圆括号周围没有空白。


## 2 类

<font color=red>类描述了一种数据类型的全部属性，对象是根据这些描述创建的实体。</font>


>例子说明类与对象：
类：famous singers
对象：taylor swift

## 3 函数

### 3.1 函数分类
函数分为两类：
- 有返回值的函数
- 没有返回值的函数[void MyFunction（）]

```C++
int rand(void);
int rand();
```

关键字`void`指出该函数不接受任何参数。<br>如果省略void，则C++将其解释为一个不接受任何参数的隐式声明。<br>在原型中使用void，如`void MyFunction（）`，来指定返回类型，以指出函数没有返回值。


### 3.2 自定义函数

#### 3.2.1 函数格式
```C++
type functionname(arqumentlist)
{
    statements
}
```

