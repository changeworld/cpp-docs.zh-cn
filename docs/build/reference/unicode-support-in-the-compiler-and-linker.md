---
title: 编译器和链接器中的 Unicode 支持
ms.date: 12/15/2017
f1_keywords:
- VC.Project.VCLinkerTool.UseUnicodeResponseFiles
- VC.Project.VCLibrarianTool.UseUnicodeResponseFiles
- VC.Project.VCCLCompilerTool.UseUnicodeResponseFiles
- VC.Project.VCXDCMakeTool.UseUnicodeResponseFiles
helpviewer_keywords:
- Unicode, Visual C++
ms.openlocfilehash: cb21165e51960c0ca2f728381413c1a7260c9f83
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/31/2018
ms.locfileid: "50494973"
---
# <a name="unicode-support-in-the-compiler-and-linker"></a>编译器和链接器中的 Unicode 支持

大多数 Visual c + + 生成工具支持 Unicode 输入和输出。

## <a name="filenames"></a>文件名

在命令行上或编译器指令中指定的文件名 (如`#include`) 可能包含 Unicode 字符。

## <a name="source-code-files"></a>源代码文件

在标识符、 宏、 字符串和字符文本和注释支持 Unicode 字符。  也支持通用字符名称。

Unicode 可以输入到源代码文件中的以下编码：

- 具有或没有字节顺序标记 (BOM) utf-16 小 endian

- 带有或不带 BOM utf-16 大 endian

- 具有 BOM 的 utf-8

## <a name="output"></a>输出

在编译期间，编译器将诊断输出到控制台以 utf-16。  可以在控制台中显示的字符取决于控制台窗口属性。  编译器输出重定向到一个文件位于当前 ANSI 控制台代码页。

## <a name="linker-response-files-and-def-files"></a>链接器响应文件和。DEF 文件

响应文件和 DEF 文件可以是任一 utf-16 BOM，或 ANSI。

## <a name="asm-and-cod-dumps"></a>.asm 和.cod 转储

.asm 和.cod 转储为 ANSI 默认情况下，以便兼容 MASM。 使用[/fau 则](../../build/reference/fa-fa-listing-file.md)输出 utf-8。 请注意，如果您指定 **/FAs**，混合的源只直接输出和可能看起来出现乱码，例如，如果源代码为 utf-8 并且未指定 **/fasu 时**。

## <a name="see-also"></a>请参阅

[在命令行上生成 C/C++ 代码](../../build/building-on-the-command-line.md)