---
title: 4.2 OMP_NUM_THREADS
ms.date: 11/04/2016
ms.assetid: 49dd55dd-25d5-4a5a-a998-cc7f47b2dae2
ms.openlocfilehash: 88ddfc226b8ae905e026e2f0979e07581d1ae83b
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/31/2018
ms.locfileid: "50668203"
---
# <a name="42-ompnumthreads"></a>4.2 OMP_NUM_THREADS

**OMP_NUM_THREADS**环境变量设置默认线程在执行期间，使用数，除非通过调用显式更改该数字**omp_set_num_threads**库例程或通过显式**num_threads**上的子句**并行**指令。

值**OMP_NUM_THREADS**环境变量必须为正整数。 其效果取决于是否启用了动态调整线程数。 获取完整的有关之间的交互的规则集**OMP_NUM_THREADS**环境变量和动态调整线程，请参阅第 8 页上的部分 2.3。

如果为不指定任何值**OMP_NUM_THREADS**环境变量，或如果指定的值不是一个正整数，或者如果值大于最大线程数系统可以支持，要使用的线程数是实现定义的。

示例:

```
setenv OMP_NUM_THREADS 16
```

## <a name="cross-references"></a>交叉引用：

- **num_threads**子句，请参阅[2.3 节](../../parallel/openmp/2-3-parallel-construct.md)第 8 页。

- **omp_set_num_threads**函数中，请参阅[部分 3.1.1](../../parallel/openmp/3-1-1-omp-set-num-threads-function.md)第 36 页上。

- **omp_set_dynamic**函数中，请参阅[部分 3.1.7](../../parallel/openmp/3-1-7-omp-set-dynamic-function.md)第 39 页上。