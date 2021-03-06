---
title: C/C++ 生成工具
ms.date: 11/04/2016
f1_keywords:
- c.build
helpviewer_keywords:
- builds [C++], C/C++ tools
- tools [C++], build
ms.assetid: 48d9daf4-6bbf-473a-8ce2-bf2923b69f80
ms.openlocfilehash: dd698aafca3c9bc489405e0ab9cb4dcec98a26ff
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/31/2018
ms.locfileid: "50510079"
---
# <a name="cc-build-tools"></a>C/C++ 生成工具

Visual c + + 提供了用于查看或操作生成输出的以下命令行工具：

- [BSCMAKE。EXE](../../build/reference/bscmake-reference.md)生成浏览信息文件 (.bsc) 包含在程序中的符号 （类、 函数、 数据、 宏和类型） 的信息。 在开发环境内的浏览窗口中查看此信息。 （.bsc 文件也可以生成在开发环境中。）

- [LIB。EXE](../../build/reference/lib-reference.md)用于创建和管理通用对象文件格式 (COFF) 对象文件的库。 它还可以用来创建导出文件和导入库，以便引用导出的定义。

- [EDITBIN。EXE](../../build/reference/editbin-reference.md)用于修改 COFF 二进制文件。

- [DUMPBIN。EXE](../../build/reference/dumpbin-reference.md)显示 COFF 二进制文件 （例如，符号表） 上的信息。

- [NMAKE](../../build/nmake-reference.md)读取并执行生成文件。

- [ERRLOOK](../../build/reference/value-edit-control.md)，错误查找实用工具检索系统错误消息或模块错误消息根据输入的值。

## <a name="see-also"></a>请参阅

[C/C++ 生成参考](../../build/reference/c-cpp-building-reference.md)<br/>
[修饰名](../../build/reference/decorated-names.md)<br/>
[编译器选项](../../build/reference/compiler-options.md)<br/>
[链接器选项](../../build/reference/linker-options.md)