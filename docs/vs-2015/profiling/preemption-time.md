---
title: 抢占时间 | Microsoft Docs
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
- vs.cv.threads.timeline.preemption
helpviewer_keywords:
- Concurrency Visualizer, Preemption Time
ms.assetid: 6b78f91e-a006-440c-83fb-e7368040951d
caps.latest.revision: 11
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 614b049bf7aa881ce4454d8f832190b0391ff342
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/22/2018
ms.locfileid: "47482954"
---
# <a name="preemption-time"></a>抢占时间
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

本主题的最新版本，请参阅[抢占时间](https://docs.microsoft.com/visualstudio/profiling/preemption-time)。  
  
时间线中的这些段与归类为“抢占”的阻塞时间关联。 此类别表示由于以下原因之一断开线程：  
  
-   计划程序使用更高优先级的线程将其替换。  
  
-   线程的执行量程过期，且其他线程已作好执行准备。  
  
 在此时间内，由于并发可视化工具被视为“抢占”这一内核等待原因，已阻止线程。 当线程被排出逻辑核心时，抢占段开始；当线程继续执行时，抢占段结束。  
  
 抢占段的工具提示会显示导致抢占的进程或线程的名称。 然而，这并不表示接管的进程或线程在抢占期间内会实际运行。  
  
## <a name="see-also"></a>请参阅  
 [线程视图](../profiling/threads-view-parallel-performance.md)


