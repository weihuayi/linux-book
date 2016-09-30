# CMake

CMake 是一个跨平台的软件构建工具, 可以极大简化软件的构建管理.


## gcc/g++ 编译器 

gcc 与 g++ 的区别: 

```
$ g++  file_name.cpp
$ g++  file_name.cpp -o test
$ g++ -O1  filen_name_cpp -o test # 优化编译, 共有 1, 2, 3 三个级别
```

给定一个程序文件, 编译成二进制程序的过程是什么?

1. 编译 
1. 链接

1. 动态库: libstdc++.so.6
1. 静态库: libcgm.a 

头文件

## make 工具

**Makefile** is a program building tool which runs on Unix, Linux, and their flavors. It
aids in simplifying building program executables that may need various modules. To
determine how the modules need to be compiled or recompiled together, make takes the
help of user-defined makefiles.

Makefile 文件的基本写法.

## CMake 工具

CMake is an extensible, open-source system that manages the build process in an
operating system and in a compiler-independent manner. Unlike many cross-platform
systems, CMake is designed to be used in conjunction with the native build
environment.

用户需要编写 CMakeLists.txt

## 基本概念

1. 变量
1. 函数
1. 流程控制语句

