---
title: c++学习心得体会
cover: https://imgs.699pic.com/images/600/027/685.jpg!detail.v1
date: 2023-10-15 09:03:00
tags:
  - 教程

categories: 技术
---
## c++学习心得

# C++基础语法完全指南

## 一、基本结构

每个C++程序都包含以下基本结构：

```cpp
#include <iostream> // 头文件包含

int main() { // 主函数，程序入口
    std::cout << "Hello, World!"; // 输出语句
    return 0; // 返回值
}
```

## 二、变量与数据类型

### 1. 基本数据类型

| 类型        | 描述                  | 大小(字节) | 示例           |
|-------------|---------------------|------------|----------------|
| `int`       | 整型                 | 4          | `int age = 25;`|
| `float`     | 单精度浮点型          | 4          | `float pi = 3.14f;`|
| `double`    | 双精度浮点型          | 8          | `double pi = 3.141592;`|
| `char`      | 字符型               | 1          | `char grade = 'A';`|
| `bool`      | 布尔型               | 1          | `bool isTrue = true;`|
| `void`      | 无类型               | -          | 用于函数返回值|

### 2. 变量声明与初始化

```cpp
int a;          // 声明
a = 10;         // 赋值
int b = 20;     // 声明并初始化
int c(30);      // 构造函数式初始化(C++11前)
int d{40};      // 统一初始化(C++11起)
auto e = 3.14;  // 自动类型推导(C++11起)
```

## 三、运算符

### 1. 算术运算符

```cpp
int x = 10, y = 3;
x + y; // 13 加法
x - y; // 7  减法
x * y; // 30 乘法
x / y; // 3  整数除法
x % y; // 1  取模
x++;   // 后置递增(返回10，x变为11)
++x;   // 前置递增(x变为12，返回12)
```

### 2. 关系运算符

```cpp
x == y; // false 等于
x != y; // true  不等于
x > y;  // true  大于
x < y;  // false 小于
x >= y; // true  大于等于
x <= y; // false 小于等于
```

### 3. 逻辑运算符

```cpp
bool a = true, b = false;
a && b; // false 逻辑与
a || b; // true  逻辑或
!a;     // false 逻辑非
```

## 四、控制结构

### 1. 条件语句

```cpp
// if语句
if (x > y) {
    std::cout << "x is greater";
} else if (x == y) {
    std::cout << "x equals y";
} else {
    std::cout << "y is greater";
}

// switch语句
char grade = 'B';
switch (grade) {
    case 'A':
        std::cout << "Excellent";
        break;
    case 'B':
        std::cout << "Good";  // 这里会执行
        break;
    default:
        std::cout << "Invalid";
}
```

### 2. 循环结构

```cpp
// while循环
int i = 0;
while (i < 5) {
    std::cout << i << " ";
    i++;
} // 输出: 0 1 2 3 4

// do-while循环
i = 0;
do {
    std::cout << i << " ";
    i++;
} while (i < 5); // 输出: 0 1 2 3 4

// for循环
for (int j = 0; j < 5; j++) {
    std::cout << j << " ";
} // 输出: 0 1 2 3 4

// 范围for循环(C++11起)
int arr[] = {1, 2, 3};
for (int num : arr) {
    std::cout << num << " ";
} // 输出: 1 2 3
```

## 五、函数基础

### 1. 函数定义与调用

```cpp
// 函数声明(原型)
int add(int a, int b);

// 函数定义
int add(int a, int b) {
    return a + b;
}

// 函数调用
int result = add(3, 4); // result = 7
```

### 2. 参数传递方式

```cpp
// 值传递(创建副本)
void changeVal(int x) { x = 10; }

// 引用传递(操作原变量)
void changeRef(int &x) { x = 10; }

// 指针传递(操作原变量)
void changePtr(int *x) { *x = 10; }

int num = 5;
changeVal(num);  // num仍为5
changeRef(num);  // num变为10
changePtr(&num); // num变为10
```

## 六、数组与字符串

### 1. 数组

```cpp
// 一维数组
int nums[5] = {1, 2, 3, 4, 5};

// 二维数组
int matrix[2][3] = {
    {1, 2, 3},
    {4, 5, 6}
};

// 访问元素
int x = nums[0];    // 1
int y = matrix[1][2]; // 6
```

### 2. 字符串

```cpp
// C风格字符串
char str1[] = "Hello";

// C++ string类
#include <string>
std::string str2 = "World";

// 字符串操作
str2.length();      // 5
str2 += "!";        // "World!"
str1 == str2;       // false
str2.substr(1, 3);  // "orl"
```

## 七、结构体

```cpp
// 定义结构体
struct Person {
    std::string name;
    int age;
    float height;
};

// 创建结构体变量
Person p1;
p1.name = "Alice";
p1.age = 25;
p1.height = 1.68f;

// 初始化结构体
Person p2 = {"Bob", 30, 1.75f};
```

## 八、基础输入输出

```cpp
#include <iostream>

int main() {
    int age;
    std::string name;
    
    // 输出
    std::cout << "Enter your name: ";
    
    // 输入字符串
    std::cin >> name;  // 读取单个单词
    // 或
    std::getline(std::cin, name); // 读取整行
    
    std::cout << "Enter your age: ";
    // 输入数字
    std::cin >> age;
    
    // 格式化输出
    std::cout << "Hello, " << name 
              << "! You are " << age 
              << " years old." << std::endl;
    
    return 0;
}
```

## 九、基础编程建议

1. **命名规范**：使用有意义的变量名，如`studentCount`而非`s`
2. **代码注释**：解释复杂逻辑，但避免过度注释
3. **缩进与格式**：保持一致的代码风格
4. **错误处理**：检查用户输入的有效性
5. **常量使用**：用`const`定义不应改变的值

```cpp
const double PI = 3.1415926;
const int MAX_SIZE = 100;
```

掌握这些基础语法后，您就可以开始编写简单的C++程序了。下一步可以学习面向对象编程、指针和内存管理等进阶概念。
