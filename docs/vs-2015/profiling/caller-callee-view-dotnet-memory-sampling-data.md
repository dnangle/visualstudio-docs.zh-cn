---
title: “调用方 - 被调用方”视图 - .NET 内存采样数据 | Microsoft Docs
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- Caller/Callee view
ms.assetid: 36f5b4de-5686-4f40-9e72-f4aee27d833c
caps.latest.revision: 17
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 04ba2a522c6accb9dcb5e316ea8c63beb260e739
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/22/2018
ms.locfileid: "47477189"
---
# <a name="callercallee-view---net-memory-sampling-data"></a>“调用方/被调用方”视图 - .NET 内存采样数据
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

本主题的最新版本，请参阅[调用方-被调用方视图-.NET 内存采样数据](https://docs.microsoft.com/visualstudio/profiling/caller-callee-view-dotnet-memory-sampling-data)。  
  
“调用方/被调用方”视图显示所选函数及其父函数和子函数的 .NET 内存分析数据。 “调用方/被调用方”视图包含三个网格。  
  
 **当前函数**在中间网格中显示，并且显示所选函数的内存分析信息。 这些值包括对函数的所有采样调用。  
  
 **调用当前函数的函数**在顶部网格中显示，并且显示由调用方（父）函数的调用生成的所选（当前）函数的值的量。  
  
 **由当前函数调用的函数**在底部网格中显示，并且在当前函数调用子函数时，它显示所选函数的被调用方（子）函数的内存分析数据。  
  
 双击调用方或被调用方函数行，以使该行成为当前函数。  
  
|列|描述|  
|------------|-----------------|  
|**进程 ID**|分析运行的进程 ID (PID)。|  
|**进程名**|进程的名称。|  
|**模块名**|函数所在模块的名称。|  
|**模块路径**|函数所在模块的路径。|  
|**源文件**|此函数的定义所在的源文件。|  
|**函数名**|该函数的完全限定名。|  
|**函数行号**|此函数在源文件中的起始行号。|  
|**函数地址**|函数的地址。|  
|**Type**|函数的上下文：<br /><br /> **0** - 当前函数<br /><br /> **1** - 调用当前函数的函数<br /><br /> **2** - 当前函数调用的函数<br /><br /> 仅在 [VSPerfReport](../profiling/vsperfreport.md) 命令行报表中。|  
|**级别**|此函数在调用树中的深度。 仅在 [VSPerfReport](../profiling/vsperfreport.md) 命令行报表中。|  
|**非独占分配数**|-   对于当前函数，是分析运行期间函数分配的对象数。 此数值包括被调用方函数中创建的对象。<br />-   对于调用方函数，是此函数的调用生成的当前函数的非独占分配数。<br />-   对于被调用方函数，是由当前函数调用的此函数的实例所分配的对象数。 此数值包括被调用方函数调用的函数所进行的分配。|  
|**非独占分配数百分比**|分析运行期间创建的属于此函数的非独占分配的所有对象数的百分比。|  
|**独占分配数**|-   对于当前函数，是函数执行函数体的代码时（即函数位于调用堆栈顶部时）创建的对象数。 此数值不包括此函数调用的函数中创建的对象数。<br />-   对于调用方函数，是此函数的调用生成的当前函数的独占分配数。<br />-   对于被调用方函数，是由当前函数调用的此函数的实例所创建的对象数。 此数值不包括被调用方函数调用的函数所创建的对象数。|  
|**独占分配数百分比**|分析运行期间创建的属于此函数的非独占分配的所有对象数的百分比。|  
|**非独占字节数**|-   对于当前函数，是分析运行期间函数分配的内存字节数。 此数值包括此函数调用的函数中所分配的内存数。<br />-   对于调用方函数，是调用方函数从调用中生成的当前函数的非独占字节数。<br />-   对于被调用方函数，是由当前函数的调用生成的此函数的实例所分配的字节数。 此数值包括被调用方函数调用的函数所分配的字节数。|  
|**非独占字节数百分比**|分析运行期间分配的属于此函数的非独占分配的所有内存字节数的百分比。|  
|**独占字节数**|-   对于当前函数，是分析运行期间函数分配的内存字节数。 此数值不包括当前函数调用的函数所分配的内存。<br />-   对于调用方函数，是调用方函数的调用生成的当前函数的独占字节数。<br />-   对于被调用方函数，是当前函数的调用生成的函数的实例所分配的字节数。 此数值不包括被调用方函数调用的函数所分配的字节数。|  
|**独占字节数百分比**|分析运行期间分配的属于此函数的独占分配的所有内存字节数的百分比。|  
  
## <a name="see-also"></a>请参阅  
 [如何：自定义报告视图列](../profiling/how-to-customize-report-view-columns.md)   
 [“调用方/被调用方”视图 - .NET 内存检测数据](../profiling/caller-callee-view-net-memory-instrumentation-data.md)   
 [“调用方/被调用方”视图 - 采样数据](../profiling/caller-callee-view-sampling-data.md)   
 [“调用方/被调用方”视图 - 检测数据](../profiling/caller-callee-view-instrumentation-data.md)


