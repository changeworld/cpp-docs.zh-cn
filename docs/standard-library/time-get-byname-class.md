---
title: time_get_byname 类
ms.date: 11/04/2016
f1_keywords:
- xloctime/std::time_get_byname
helpviewer_keywords:
- time_get_byname class
ms.assetid: 6e54153e-da40-4bb9-a942-1a6ce57b30c9
ms.openlocfilehash: e18f210dba03d66fa3a4ea111a6dfc61f0d0c12a
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/31/2018
ms.locfileid: "50596460"
---
# <a name="timegetbyname-class"></a>time_get_byname 类

一种派生模板类，用于描述一个可充当类型 `time_get`\< CharType、InputIterator > 的区域设置 facet 的对象。

## <a name="syntax"></a>语法

```cpp
template <class Elem, class InputIterator =
    istreambuf_iterator<CharType, char_traits<CharType>>>
class time_get_byname : public time_get<CharType, InputIterator>
{
public:
    explicit time_get_byname(
    const char* _Locname,
    size_t _Refs = 0);

    explicit time_get_byname(
    const string& _Locname,
    size_t _Refs = 0);

protected:
    virtual ~time_get_byname()
};
```

### <a name="parameters"></a>参数

*_Locname*<br/>
已命名的区域设置。

*_Refs*<br/>
初始引用计数。

## <a name="requirements"></a>要求

其行为由命名的区域设置确定 *_Locname*。 每个构造函数都使用 [time_get](../standard-library/time-get-class.md#time_get)\<CharType、InputIterator>( `_Refs`) 初始化其基对象。

## <a name="requirements"></a>要求

**标头：** \<locale>

**命名空间：** std

## <a name="see-also"></a>请参阅

[C++ 标准库中的线程安全](../standard-library/thread-safety-in-the-cpp-standard-library.md)<br/>
