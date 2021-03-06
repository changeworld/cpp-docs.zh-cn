---
title: __readdr
ms.date: 11/04/2016
f1_keywords:
- __readdr
helpviewer_keywords:
- __readdr intrinsic
ms.assetid: 061b05da-c85e-4052-b392-106f14bb84f1
ms.openlocfilehash: 7e6f485eef5e3c54cb406d0c2b3abe824dbf584b
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/31/2018
ms.locfileid: "50438761"
---
# <a name="readdr"></a>__readdr

读取指定的调试寄存器的值。

## <a name="syntax"></a>语法

```
unsigned         __readdr(unsigned int DebugRegister);
unsigned __int64 __readdr(unsigned int DebugRegister);
```

#### <a name="parameters"></a>参数

*DebugRegister*<br/>
[in]从 0 到 7 标识调试常量注册。

## <a name="return-value"></a>返回值

指定的调试寄存器的值。

## <a name="remarks"></a>备注

这些内部函数仅在内核模式中可用，例程只能用作内部函数。

## <a name="requirements"></a>要求

|内部函数|体系结构|
|---------------|------------------|
|`__readdr`|x86、x64|

**标头文件** \<intrin.h >

**结束 Microsoft 专用**

## <a name="see-also"></a>请参阅

[编译器内部函数](../intrinsics/compiler-intrinsics.md)<br/>
[__readeflags](../intrinsics/readeflags.md)