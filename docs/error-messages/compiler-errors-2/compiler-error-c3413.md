---
title: 编译器错误 C3413
ms.date: 11/04/2016
f1_keywords:
- C3413
helpviewer_keywords:
- C3413
ms.assetid: de6c9b05-c373-4bd8-8cb0-12c2cd2e5674
ms.openlocfilehash: e344d06345c0f3a79b86e9cab4e1c5dacb47e9c2
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/31/2018
ms.locfileid: "50453282"
---
# <a name="compiler-error-c3413"></a>编译器错误 C3413

“name”：显式实例化无效

编译器检测到格式不正确的显式实例化。

下面的示例生成 C3413：

```
// C3413.cpp
template
class MyClass {};   // C3413
```

可能的解决方法：

```
// C3413b.cpp
// compile with: /c
template <class T>
class MyClass {};

template <>
class MyClass<int> {};
```