---
title: IDebugDynamicField |Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugDynamicField
helpviewer_keywords:
- IDebugDynamicField interface
ms.assetid: caffbd95-7596-4714-84b1-b964e89a78bb
author: acangialosi
ms.author: anthc
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 15f0ddf70849377d37ec74839550de6057b3450c
ms.sourcegitcommit: 6cfffa72af599a9d667249caaaa411bb28ea69fd
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/02/2020
ms.locfileid: "80731313"
---
# <a name="idebugdynamicfield"></a>IDebugDynamicField
此接口表示变量的类型。

## <a name="syntax"></a>语法

```
IDebugDynamicField : IDebugField
```

## <a name="notes-for-implementers"></a>实施者注意事项
 此接口由符号提供程序作为可在运行时确定的任何类型的基类实现。 这仅适用于托管代码。

## <a name="notes-for-callers"></a>调用方说明
 此接口表示一个基类，可以从该基类派生更多专用化的接口。

## <a name="methods-in-vtable-order"></a>Vtable 顺序的方法
 此接口不提供从继承的以外的任何方法 `IDebugField` 。

## <a name="requirements"></a>要求
 标头： sh。h

 命名空间： VisualStudio

 程序集： Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>另请参阅
- [符号提供程序接口](../../../extensibility/debugger/reference/symbol-provider-interfaces.md)
- [IDebugField](../../../extensibility/debugger/reference/idebugfield.md)
