---
title:      include和#import有什么作用和区别？
date:       2024-04-17
tags:
- C
- Objective-C
--- 

`#include` 和 `#import` 都是用于在C和C++程序中引入外部代码的预处理指令，它们的作用是将指定的文件内容插入到当前文件中。但是它们在使用方式和行为上有一些区别：

1. **#include**：
   - `#include` 是C和C++语言中的标准预处理指令，用于包含外部头文件的内容。
   - 语法格式：`#include <header_file>` 或 `#include "header_file"`
   - 当使用尖括号 `<>` 包含头文件时，编译器会在系统默认的目录中搜索头文件。
   - 当使用双引号 `""` 包含头文件时，编译器会先在当前源文件所在的目录中搜索头文件，如果没有找到，再去系统默认目录中搜索。
   - `#include` 没有保护机制，即使同一个头文件被包含多次，编译器也会重复插入该头文件的内容。

2. **#import**：
   - `#import` 是Objective-C语言的预处理指令，用于引入外部Objective-C类的头文件。
   - 语法格式：`#import "header_file"`
   - `#import` 和 `#include` 的功能相似，但 `#import` 在处理重复引用时会有所不同。
   - `#import` 会自动检测文件是否已经被引入，如果已经引入过，则不会再次引入，避免了重复引用带来的问题，例如循环引用。
   - 在 Objective-C 中，推荐使用 `#import` 来引入头文件，因为它提供了更好的保护机制，可以避免重复引用导致的编译错误或警告。

综上所述，`#include` 和 `#import` 都用于引入外部代码，但 `#import` 是 Objective-C 特有的，并且具有更好的重复引用保护机制，而 `#include` 是 C 和 C++ 的标准预处理指令，在使用方式和行为上略有不同。