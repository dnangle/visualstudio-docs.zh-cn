---
title: IDiaFrameData::get_addressOffset | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaFrameData::get_addressOffset method
ms.assetid: b68e2e68-6483-4936-bf97-1b0a13cb75e2
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 651ff39eed19a22c1ace24453a44b38ef512b9b8
ms.sourcegitcommit: 5f6ad1cefbcd3d531ce587ad30e684684f4c4d44
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/22/2019
ms.locfileid: "72743678"
---
# <a name="idiaframedataget_addressoffset"></a>IDiaFrameData::get_addressOffset
检索帧的代码地址的偏移量部分。

## <a name="syntax"></a>语法

```C++
HRESULT get_addressOffset ( 
   DWORD* pRetVal
);
```

#### <a name="parameters"></a>参数
 `pRetVal`

弄返回帧的代码地址的偏移量部分。

## <a name="return-value"></a>返回值
 如果成功，则返回 `S_OK`。 如果此属性不受支持，则返回 `S_FALSE`。 否则，返回错误代码。

## <a name="see-also"></a>请参阅
- [IDiaFrameData](../../debugger/debug-interface-access/idiaframedata.md)