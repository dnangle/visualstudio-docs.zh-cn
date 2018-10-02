---
title: POPLISTFUNC |Microsoft Docs
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- POPDIRLISTFUNC
helpviewer_keywords:
- POPLISTFUNC callback function
ms.assetid: b2199fd5-d707-4628-92dd-e2a01e2f507a
caps.latest.revision: 17
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: a8b193eae0e41f48c0f947bbf8af596084a1544f
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/22/2018
ms.locfileid: "47482539"
---
# <a name="poplistfunc"></a>POPLISTFUNC
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

本主题的最新版本，请参阅[POPLISTFUNC](https://docs.microsoft.com/visualstudio/extensibility/poplistfunc)。  
  
此回调提供给[SccPopulateList](../extensibility/sccpopulatelist-function.md) ide 和源代码管理插件用于更新的文件或目录的列表 (还提供给`SccPopulateList`函数)。  
  
 当用户选择**获取**命令在 IDE 中，则 IDE 将显示一个列表框，用户可以获取的所有文件。 遗憾的是，IDE 不知道用户可能会收到; 的所有文件的确切列表仅插件都有此列表。 如果其他用户将文件添加到源代码管理项目，这些文件应出现在列表中，但 IDE 并不了解它们。 在 IDE 中生成它认为用户可以获取文件的列表。 它为用户显示此列表之前，它将调用[SccPopulateList](../extensibility/sccpopulatelist-function.md) `,`为源代码管理插件提供机会进行添加并从列表中删除文件。  
  
## <a name="signature"></a>签名  
 源代码管理插件修改通过调用带以下原型的 IDE 实现函数的列表：  
  
```cpp#  
typedef BOOL (*POPLISTFUNC) (  
   LPVOID pvCallerData,  
   BOOL fAddRemove,  
   LONG nStatus,  
   LPSTR lpFileName  
);  
```  
  
## <a name="parameters"></a>参数  
 pvCallerData  
 `pvCallerData`参数由调用方 (IDE) 传递给[SccPopulateList](../extensibility/sccpopulatelist-function.md)。 源代码管理插件应假定不了解此参数的内容。  
  
 fAddRemove  
 如果`TRUE`，`lpFileName`是一个文件，应添加到的文件列表。 如果`FALSE`，`lpFileName`是应从文件列表中删除的文件。  
  
 nStatus  
 状态`lpFileName`(的组合`SCC_STATUS`位，请参见[文件状态代码](../extensibility/file-status-code-enumerator.md)有关详细信息)。  
  
 lpFileName  
 要添加或从列表中删除的文件名称的完整目录路径。  
  
## <a name="return-value"></a>返回值  
  
|“值”|描述|  
|-----------|-----------------|  
|`TRUE`|该插件可以继续调用此函数。|  
|`FALSE`|在 IDE 端 （如不足的内存情况下） 已出现问题。 插件应停止操作。|  
  
## <a name="remarks"></a>备注  
 对于每个源代码管理插件想要添加到或从文件列表中删除的文件，它将调用此函数，并传入`lpFileName`。 `fAddRemove`标志指示要添加到列表中的新文件或要删除的旧文件。 `nStatus`参数指定了文件的状态。 当插件 SCC 完成添加和删除文件时，它将返回[SccPopulateList](../extensibility/sccpopulatelist-function.md)调用。  
  
> [!NOTE]
>  `SCC_CAP_POPULATELIST`功能位是所必需的 Visual Studio。  
  
## <a name="see-also"></a>请参阅  
 [通过 IDE 实现的回调函数](../extensibility/callback-functions-implemented-by-the-ide.md)   
 [源代码管理插件](../extensibility/source-control-plug-ins.md)   
 [SccPopulateList](../extensibility/sccpopulatelist-function.md)   
 [文件状态代码](../extensibility/file-status-code-enumerator.md)
