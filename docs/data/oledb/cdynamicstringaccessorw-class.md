---
title: CDynamicStringAccessorW 类
ms.date: 11/04/2016
f1_keywords:
- CDynamicStringAccessorW
helpviewer_keywords:
- CDynamicStringAccessorW class
ms.assetid: 9b7fd5cc-3a9b-4b57-b907-f1e35de2c98f
ms.openlocfilehash: 7052a912363d1256294131da9b89df97f768ecf8
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/31/2018
ms.locfileid: "50551354"
---
# <a name="cdynamicstringaccessorw-class"></a>CDynamicStringAccessorW 类

可以在不知道数据库架构 （基础结构） 时访问数据源。

## <a name="syntax"></a>语法

```cpp
typedef CDynamicStringAccessorT<WCHAR, DBTYPE_WSTR> CDynamicStringAccessorW;
```

## <a name="remarks"></a>备注

在这两个请求提供程序提取从字符串数据作为数据存储区访问的所有数据，但`CDynamicStringAccessor`请求 Unicode 字符串数据。

`CDynamicStringAccessorW` 继承`GetString`并`SetString`从`CDynamicStringAccessor`。 使用这些方法时`CDynamicStringAccessorW`对象，`BaseType`是**WCHAR**。

## <a name="requirements"></a>要求

**标头**：atldbcli.h

## <a name="see-also"></a>请参阅

[OLE DB 使用者模板](../../data/oledb/ole-db-consumer-templates-cpp.md)<br/>
[OLE DB 使用者模板参考](../../data/oledb/ole-db-consumer-templates-reference.md)<br/>
[CAccessor 类](../../data/oledb/caccessor-class.md)<br/>
[CDynamicParameterAccessor 类](../../data/oledb/cdynamicparameteraccessor-class.md)<br/>
[CManualAccessor 类](../../data/oledb/cmanualaccessor-class.md)<br/>
[CDynamicAccessor 类](../../data/oledb/cdynamicaccessor-class.md)<br/>
[CDynamicStringAccessor 类](../../data/oledb/cdynamicstringaccessor-class.md)<br/>
