---
title: IDBCreateSessionImpl 类
ms.date: 11/04/2016
f1_keywords:
- IDBCreateSessionImpl
- ATL.IDBCreateSessionImpl
- ATL::IDBCreateSessionImpl
- IDBCreateSessionImpl::CreateSession
- IDBCreateSessionImpl.CreateSession
- CreateSession
helpviewer_keywords:
- IDBCreateSessionImpl class
- CreateSession method
ms.assetid: 48c02c5c-8362-45ac-af8e-bb119cf8c5c7
ms.openlocfilehash: ecc06bf5e3514ea87c86de17dbafd59b9da9f8b6
ms.sourcegitcommit: c40469825b6101baac87d43e5f4aed6df6b078f5
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/12/2018
ms.locfileid: "51556417"
---
# <a name="idbcreatesessionimpl-class"></a>IDBCreateSessionImpl 类

提供一个实现[IDBCreateSession](https://docs.microsoft.com/previous-versions/windows/desktop/ms724076(v=vs.85))接口。

## <a name="syntax"></a>语法

```cpp
template <class T, class SessionClass>
class ATL_NO_VTABLE IDBCreateSessionImpl
   : public IDBCreateSession
```

### <a name="parameters"></a>参数

*T*<br/>
您的类，派生自

*SessionClass*<br/>
会话对象中。

## <a name="requirements"></a>要求

**标头：** atldb.h

## <a name="members"></a>成员

### <a name="interface-methods"></a>接口方法

|||
|-|-|
|[CreateSession](#createsession)|从数据源对象创建一个新的会话并返回所请求的接口上新创建的会话。|

## <a name="remarks"></a>备注

数据源对象上的必需接口。

## <a name="createsession"></a> Idbcreatesessionimpl:: Createsession

从数据源对象创建一个新的会话并返回所请求的接口上新创建的会话。

### <a name="syntax"></a>语法

```cpp
STDMETHOD(CreateSession)(IUnknown * pUnkOuter,
   REFIID riid,
   IUnknown ** ppDBSession);
```

#### <a name="parameters"></a>参数

请参阅[idbcreatesession:: Createsession](https://docs.microsoft.com/previous-versions/windows/desktop/ms714942(v=vs.85))中*OLE DB 程序员参考*。

## <a name="see-also"></a>请参阅

[OLE DB 提供程序模板](../../data/oledb/ole-db-provider-templates-cpp.md)<br/>
[OLE DB 提供程序模板体系结构](../../data/oledb/ole-db-provider-template-architecture.md)