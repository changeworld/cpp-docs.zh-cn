---
title: 编译器错误 C2462
ms.date: 11/04/2016
f1_keywords:
- C2462
helpviewer_keywords:
- C2462
ms.assetid: a8601bf8-f5ce-41de-9117-e2632bd4996b
ms.openlocfilehash: 0b342f8b878c48a77336fab4921cf4a668e248ab
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/31/2018
ms.locfileid: "50607046"
---
# <a name="compiler-error-c2462"></a>编译器错误 C2462

identifier： 无法在 new-expression 中定义类型

不能定义一种类型的操作数字段中`new`运算符。 将类型定义放在一个单独的语句。

下面的示例生成 C2462:

```
// C2462.cpp
int main() {
   new struct S { int i; };   // C2462
}
```