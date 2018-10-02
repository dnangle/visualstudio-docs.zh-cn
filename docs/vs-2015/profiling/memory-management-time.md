---
title: 内存管理时间 | Microsoft Docs
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- vs.cv.threads.timeline.paging
helpviewer_keywords:
- Concurrency Visualizer, Paging Time
ms.assetid: 67af3509-3a7d-435d-bc37-5262448da915
caps.latest.revision: 14
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 9371c4d5249539c80299fd1b1573eba19c9dd14f
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/22/2018
ms.locfileid: "47469110"
---
# <a name="memory-management-time"></a>内存管理时间
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

本主题的最新版本，请参阅[内存管理时间](https://docs.microsoft.com/visualstudio/profiling/memory-management-time)。  
  
时间线中的这些段与归类为内存管理的阻塞时间关联。 这意味着线程被与内存管理操作（如分页）关联的事件所阻止。 在此时间内，线程被阻止在并发可视化工具视为内存管理的 API 或内核状态下。 这些包括诸如分页和内存分配这类事件。  
  
 检查关联的调用堆栈和分析报告，以便更好地了解归类为内存管理的阻塞的基本原因。  
  
## <a name="see-also"></a>请参阅  
 [线程视图](../profiling/threads-view-parallel-performance.md)


