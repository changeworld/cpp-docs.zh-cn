---
title: include_alias
ms.date: 11/04/2016
f1_keywords:
- vc-pragma.include_alias
- include_alias_CPP
helpviewer_keywords:
- pragmas, include_alias
- include_alias pragma
ms.assetid: 3256d589-12b3-4af0-a586-199e96eabacc
ms.openlocfilehash: 616672d713a9f0ac6eab4be8bce9b178d2510723
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/31/2018
ms.locfileid: "50573157"
---
# <a name="includealias"></a>include_alias

指定的*short_filename*是要用作别名*long_filename*。

## <a name="syntax"></a>语法

> #<a name="pragma-includealiaslongfilename-shortfilename"></a>include_alias 杂注 ("*long_filename*"，"*short_filename*")
> #<a name="pragma-includealiaslongfilename-shortfilename"></a>include_alias 杂注 (*long_filename*， *short_filename*)

## <a name="remarks"></a>备注

某些文件系统允许长度超过 8.3 FAT 文件系统限制的头文件名。 因为较长的头文件名的前八个字符可能不是唯一的，因此编译器无法简单地将较长的名称截断为 8.3。 每当编译器遇到*long_filename*字符串，它将替代*short_filename*，并查找标头文件*short_filename*相反。 此杂注必须在相应的 `#include` 指令之前出现。 例如：

```cpp
// First eight characters of these two files not unique.
#pragma include_alias( "AppleSystemHeaderQuickdraw.h", "quickdra.h" )
#pragma include_alias( "AppleSystemHeaderFruit.h", "fruit.h" )

#pragma include_alias( "GraphicsMenu.h", "gramenu.h" )

#include "AppleSystemHeaderQuickdraw.h"
#include "AppleSystemHeaderFruit.h"
#include "GraphicsMenu.h"
```

要搜索的别名必须完全符合规范，无论是大小写、拼写还是双引号或尖括号的使用。 **Include_alias**杂注执行简单的字符串匹配对文件名; 不执行任何其他文件名验证。 例如，给定下列指令，

```cpp
#pragma include_alias("mymath.h", "math.h")
#include "./mymath.h"
#include "sys/mymath.h"
```

将不执行指定别名（替换）操作，因为头文件字符串不完全匹配。 此外，用作自变量的头文件名`/Yu`并`/Yc`编译器选项或`hdrstop`杂注时，将不会替换。 例如，如果源文件包含以下指令，

```cpp
#include <AppleSystemHeaderStop.h>
```

则相应的编译器选项应为

> /YcAppleSystemHeaderStop.h

可以使用**include_alias**杂注将任何标头文件名映射到另一个。 例如：

```cpp
#pragma include_alias( "api.h", "c:\version1.0\api.h" )
#pragma include_alias( <stdio.h>, <newstdio.h> )
#include "api.h"
#include <stdio.h>
```

不要将用双引号括起来的文件名与用尖括号括起的文件名组合在一起。 例如，给定上述两个`#pragma include_alias`指令，编译器对以下执行任何替换`#include`指令：

```cpp
#include <api.h>
#include "stdio.h"
```

而且，以下指令将生成错误：

```cpp
#pragma include_alias(<header.h>, "header.h")  // Error
```

请注意，文件名报告错误消息中或作为预定义值`__FILE__`宏，在执行替换后的文件的名称。 例如，以下指令后看到输出：

```cpp
#pragma include_alias( "VeryLongFileName.H", "myfile.h" )
#include "VeryLongFileName.H"
```

VERYLONGFILENAME 中的错误。H 生成以下错误消息：

```Output
myfile.h(15) : error C2059 : syntax error
```

请注意，不支持传递性。 给定以下指令，

```cpp
#pragma include_alias( "one.h", "two.h" )
#pragma include_alias( "two.h", "three.h" )
#include "one.h"
```

编译器将搜索文件 TWO.H 而不是 THREE.H。

## <a name="see-also"></a>请参阅

[Pragma 指令和 __Pragma 关键字](../preprocessor/pragma-directives-and-the-pragma-keyword.md)