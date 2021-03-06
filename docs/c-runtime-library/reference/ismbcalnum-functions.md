---
title: _ismbcalnum、_ismbcalnum_l、_ismbcalpha、_ismbcalpha_l、_ismbcdigit、_ismbcdigit_l
ms.date: 11/04/2016
apiname:
- _ismbcalpha
- _ismbcalnum
- _ismbcdigit
- _ismbcalnum_l
- _ismbcdigit_l
- _ismbcalpha_l
apilocation:
- msvcrt.dll
- msvcr80.dll
- msvcr90.dll
- msvcr100.dll
- msvcr100_clr0400.dll
- msvcr110.dll
- msvcr110_clr0400.dll
- msvcr120.dll
- msvcr120_clr0400.dll
- ucrtbase.dll
- api-ms-win-crt-multibyte-l1-1-0.dll
apitype: DLLExport
f1_keywords:
- _ismbcdigit
- ismbcalnum_l
- _ismbcdigit_l
- _ismbcalpha
- ismbcalnum
- ismbcdigit
- ismbcalpha
- _ismbcalnum_l
- _ismbcalnum
- ismbcdigit_l
helpviewer_keywords:
- ismbcalpha function
- _ismbcalnum function
- ismbcdigit_l function
- _ismbcalnum_l function
- _ismbcdigit function
- ismbcalnum function
- _ismbcalpha_l function
- ismbcdigit function
- _ismbcalpha function
- _ismbcdigit_l function
- ismbcalnum_l function
- ismbcalpha_l function
ms.assetid: 12d57925-aebe-46e0-80b0-82b84c4c31ec
ms.openlocfilehash: 1a2f928d826b70b788220130f69c53cc351b4910
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/31/2018
ms.locfileid: "50532218"
---
# <a name="ismbcalnum-ismbcalnuml-ismbcalpha-ismbcalphal-ismbcdigit-ismbcdigitl"></a>_ismbcalnum、_ismbcalnum_l、_ismbcalpha、_ismbcalpha_l、_ismbcdigit、_ismbcdigit_l

检查多字节字符是字母数字字符、alpha 还是数字字符。

> [!IMPORTANT]
> 此 API 不能用于在 Windows 运行时中执行的应用程序。 有关详细信息，请参阅[通用 Windows 平台应用中不支持的 CRT 函数](../../cppcx/crt-functions-not-supported-in-universal-windows-platform-apps.md)。

## <a name="syntax"></a>语法

```C
int _ismbcalnum
(
   unsigned int c
);
int _ismbcalnum_l
(
   unsigned int c,
   _locale_t locale
);
int _ismbcalpha
(
   unsigned int c
);
int _ismbcalpha_l
(
   unsigned int c,
   _locale_t locale
);
int _ismbcdigit
(
   unsigned int c
);
int _ismbcdigit_l
(
   unsigned int c,
   _locale_t locale
);
```

### <a name="parameters"></a>参数

*c*<br/>
要测试的字符。

*locale*<br/>
要使用的区域设置。

## <a name="return-value"></a>返回值

其中每个例程在字符满足测试条件时返回一个非零值，在不满足测试条件时回 0。 如果*c*< = 255 且存在相应 **_ismbb**例程 (例如， **_ismbcalnum**对应于 **_ismbbalnum**)，则结果是相应的返回值 **_ismbb**例程。

## <a name="remarks"></a>备注

其中每个例程都针对给定的条件测试给定的多字节字符。

使用这些函数的版本 **_l**后缀完全相同，只不过它们使用为其区域设置相关的行为而不是当前区域设置传入的区域设置。 有关详细信息，请参阅 [Locale](../../c-runtime-library/locale.md)。

|例程所返回的值|测试条件|代码页 932 示例|
|-------------|--------------------|---------------------------|
|**_ismbcalnum**， **_ismbcalnum_l**|字母数字|返回非零值，当且仅当*c*是 ASCII 英文字母的单字节表示形式： 请参阅示例 **_ismbcdigit**并 **_ismbcalpha**。|
|**_ismbcalpha**， **_ismbcalpha_l**|Alphabetic|返回非零值，当且仅当*c*是 ASCII 英文字母的单字节表示形式： 0x41 < =*c*< = 0x5A 或 0x61 < =*c*< = 0x7A; 或是片假名字母：0xa6< < =*c*< = 0xDF。|
|**_ismbcdigit**， **_ismbcdigit**|数字|返回非零值，当且仅当*c*是 ASCII 数字的单字节表示形式： 0x30 < =*c*< = 0x39。|

## <a name="requirements"></a>要求

|例程所返回的值|必需的标头|
|-------------|---------------------|
|**_ismbcalnum**， **_ismbcalnum_l**|\<mbstring.h>|
|**_ismbcalpha**， **_ismbcalpha_l**|\<mbstring.h>|
|**_ismbcdigit**， **_ismbcdigit_l**|\<mbstring.h>|

有关更多兼容性信息，请参阅 [兼容性](../../c-runtime-library/compatibility.md)。

## <a name="see-also"></a>请参阅

[字符分类](../../c-runtime-library/character-classification.md)<br/>
[_ismbc 例程](../../c-runtime-library/ismbc-routines.md)<br/>
[is、isw 例程](../../c-runtime-library/is-isw-routines.md)<br/>
[_ismbb 例程](../../c-runtime-library/ismbb-routines.md)<br/>
