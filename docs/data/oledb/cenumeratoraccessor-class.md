---
title: CEnumeratorAccessor 类
ms.date: 11/04/2016
f1_keywords:
- ATL::CEnumeratorAccessor
- CEnumeratorAccessor
- ATL.CEnumeratorAccessor
- CEnumeratorAccessor.m_bIsParent
- ATL::CEnumeratorAccessor::m_bIsParent
- m_bIsParent
- ATL.CEnumeratorAccessor.m_bIsParent
- CEnumeratorAccessor::m_bIsParent
- ATL::CEnumeratorAccessor::m_nType
- CEnumeratorAccessor.m_nType
- CEnumeratorAccessor::m_nType
- ATL.CEnumeratorAccessor.m_nType
- m_nType
- ATL::CEnumeratorAccessor::m_szDescription
- CEnumeratorAccessor.m_szDescription
- CEnumeratorAccessor::m_szDescription
- ATL.CEnumeratorAccessor.m_szDescription
- CEnumeratorAccessor::m_szName
- ATL.CEnumeratorAccessor.m_szName
- m_szName
- ATL::CEnumeratorAccessor::m_szName
- CEnumeratorAccessor.m_szName
- CEnumeratorAccessor::m_szParseName
- ATL::CEnumeratorAccessor::m_szParseName
- m_szParseName
- CEnumeratorAccessor.m_szParseName
- ATL.CEnumeratorAccessor.m_szParseName
helpviewer_keywords:
- CEnumeratorAccessor class
- m_bIsParent
- m_nType
- m_szDescription
- m_szName
- m_szParseName
ms.assetid: 21e8e7ea-3511-4afe-b33f-d520f4ff82bb
ms.openlocfilehash: 2bcbf55c4bc6d546c8a2b4eca3ea2dbeafc613fa
ms.sourcegitcommit: c40469825b6101baac87d43e5f4aed6df6b078f5
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/12/2018
ms.locfileid: "51556343"
---
# <a name="cenumeratoraccessor-class"></a>CEnumeratorAccessor 类

通过使用[CEnumerator](../../data/oledb/cenumerator-class.md)从枚举器行集访问数据。

## <a name="syntax"></a>语法

```cpp
class CEnumeratorAccessor
```

## <a name="requirements"></a>要求

**标头:** atldbcli.h

## <a name="members"></a>成员

### <a name="data-members"></a>数据成员

|||
|-|-|
|[m_bIsParent](#bisparent)|变量，用于指示枚举器是否父级的枚举器，如果行是一个枚举器。|
|[m_nType](#ntype)|一个，该值指示是否行所说明的数据源或枚举数的变量。|
|[m_szDescription](#szdescription)|数据源或枚举器的说明。|
|[m_szName](#szname)|枚举器的数据源的名称。|
|[m_szParseName](#szparsename)|要传递给字符串[IParseDisplayName](/windows/desktop/api/oleidl/nn-oleidl-iparsedisplayname)若要获取的数据源或枚举器的名字对象。|

## <a name="remarks"></a>备注

此行包含数据源和枚举器当前枚举器中可见。

## <a name="bisparent"></a> Cenumeratoraccessor:: M_bisparent

变量，用于指示枚举器是否父级的枚举器，如果行是一个枚举器。

### <a name="syntax"></a>语法

```cpp
VARIANT_BOOL m_bIsParent;
```

### <a name="remarks"></a>备注

请参阅[isourcesrowset:: Getsourcesrowset](https://docs.microsoft.com/previous-versions/windows/desktop/ms711200(v=vs.85))中*OLE DB 程序员参考*有关详细信息。

## <a name="ntype"></a> Cenumeratoraccessor:: M_ntype

一个，该值指示是否行所说明的数据源或枚举数的变量。

### <a name="syntax"></a>语法

```cpp
USHORT m_nType;
```

### <a name="remarks"></a>备注

请参阅[isourcesrowset:: Getsourcesrowset](https://docs.microsoft.com/previous-versions/windows/desktop/ms711200(v=vs.85))中*OLE DB 程序员参考*有关详细信息。

## <a name="szdescription"></a> Cenumeratoraccessor:: M_szdescription

数据源或枚举器的说明。

### <a name="syntax"></a>语法

```cpp
WCHAR m_szDescription[129];
```

### <a name="remarks"></a>备注

请参阅[isourcesrowset:: Getsourcesrowset](https://docs.microsoft.com/previous-versions/windows/desktop/ms711200(v=vs.85))中*OLE DB 程序员参考*有关详细信息。

## <a name="szname"></a> Cenumeratoraccessor:: M_szname

枚举器的数据源的名称。

### <a name="syntax"></a>语法

```cpp
WCHAR m_szName[129];
```

### <a name="remarks"></a>备注

请参阅[isourcesrowset:: Getsourcesrowset](https://docs.microsoft.com/previous-versions/windows/desktop/ms711200(v=vs.85))中*OLE DB 程序员参考*有关详细信息。

## <a name="szparsename"></a> Cenumeratoraccessor:: M_szparsename

要传递给字符串[IParseDisplayName](/windows/desktop/api/oleidl/nn-oleidl-iparsedisplayname)若要获取的数据源或枚举器的名字对象。

### <a name="syntax"></a>语法

```cpp
WCHAR m_szParseName[129];
```

### <a name="remarks"></a>备注

请参阅[isourcesrowset:: Getsourcesrowset](https://docs.microsoft.com/previous-versions/windows/desktop/ms711200(v=vs.85))中*OLE DB 程序员参考*有关详细信息。

## <a name="see-also"></a>请参阅

[OLE DB 使用者模板](../../data/oledb/ole-db-consumer-templates-cpp.md)<br/>
[OLE DB 使用者模板参考](../../data/oledb/ole-db-consumer-templates-reference.md)