---
title: rename、_wrename
ms.date: 11/04/2016
apiname:
- rename
- _wrename
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
- api-ms-win-crt-filesystem-l1-1-0.dll
apitype: DLLExport
f1_keywords:
- _wrename
- _trename
- Rename
helpviewer_keywords:
- trename function
- directories [C++], renaming
- renaming directories
- names [C++], changing file
- _trename function
- rename function
- wrename function
- files [C++], renaming
- _wrename function
- names [C++], changing directory
- renaming files
ms.assetid: 9f0a6103-26a2-4dda-b14b-79a48946266a
ms.openlocfilehash: 3536bfb6c38c99a8d6d943102fb9303dd4d85b7b
ms.sourcegitcommit: 1819bd2ff79fba7ec172504b9a34455c70c73f10
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/09/2018
ms.locfileid: "51326129"
---
# <a name="rename-wrename"></a>rename、_wrename

重命名文件或目录。

## <a name="syntax"></a>语法

```C
int rename(
   const char *oldname,
   const char *newname
);
int _wrename(
   const wchar_t *oldname,
   const wchar_t *newname
);
```

### <a name="parameters"></a>参数

*oldname*<br/>
指向旧名称的指针。

*newname*<br/>
指向新名称的指针。

## <a name="return-value"></a>返回值

如果成功，则这些函数均返回 0。 发生错误时，该函数返回非零值，并设置**errno**为以下值之一：

|errno 值|条件|
|-|-|
| **EACCES** | 由 *newname* 指定的文件或目录已存在或无法创建（路径无效）；或 *oldname* 是目录，但 *newname* 指定了不同路径。 |
| **ENOENT** | 未找到由 *oldname* 指定的文件或路径。 |
| **EINVAL** | 名称包含无效字符。 |

有关其他可能的返回值，请参阅 [_doserrno、_errno、syserrlist 和 _sys_nerr](../../c-runtime-library/errno-doserrno-sys-errlist-and-sys-nerr.md)。

## <a name="remarks"></a>备注

**rename** 函数将 *oldname* 指定的文件或目录重命名为由 *newname* 给定的名称。 旧名称必须是现有文件或目录的路径。 新名称一定不能是现有文件或目录的名称。 通过在 *newname* 参数中给定不同的路径，可以使用 **rename** 将文件从一个目录或设备移至另一个目录或设备。 但是，不能使用 **rename** 来移动目录。 目录可以重命名，但不能移动。

**_wrename**是宽字符版本 **_rename**; 的自变量 **_wrename**都是宽字符字符串。 **_wrename**并 **_rename**行为相同。

### <a name="generic-text-routine-mappings"></a>一般文本例程映射

|TCHAR.H 例程|未定义 _UNICODE 和 _MBCS|已定义 _MBCS|已定义 _UNICODE|
|---------------------|------------------------------------|--------------------|-----------------------|
|**_trename**|**rename**|**rename**|**_wrename**|

## <a name="requirements"></a>要求

|例程所返回的值|必需的标头|
|-------------|---------------------|
|**rename**|\<io.h> 或 \<stdio.h>|
|**_wrename**|\<stdio.h> 或 \<wchar.h>|

有关其他兼容性信息，请参阅 [兼容性](../../c-runtime-library/compatibility.md)。

## <a name="libraries"></a>库

[C 运行时库](../../c-runtime-library/crt-library-features.md)的所有版本。

## <a name="example"></a>示例

```C
// crt_renamer.c
/* This program attempts to rename a file named
* CRT_RENAMER.OBJ to CRT_RENAMER.JBO. For this operation
* to succeed, a file named CRT_RENAMER.OBJ must exist and
* a file named CRT_RENAMER.JBO must not exist.
*/

#include <stdio.h>

int main( void )
{
   int  result;
   char old[] = "CRT_RENAMER.OBJ", new[] = "CRT_RENAMER.JBO";

   /* Attempt to rename file: */
   result = rename( old, new );
   if( result != 0 )
      printf( "Could not rename '%s'\n", old );
   else
      printf( "File '%s' renamed to '%s'\n", old, new );
}
```

### <a name="output"></a>输出

```Output
File 'CRT_RENAMER.OBJ' renamed to 'CRT_RENAMER.JBO'
```

## <a name="see-also"></a>请参阅

[文件处理](../../c-runtime-library/file-handling.md)<br/>
