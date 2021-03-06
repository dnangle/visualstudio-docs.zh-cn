---
title: 何时实现源代码管理 VSPackage
ms.custom: SEO-VS-2020
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- source control packages, about source control packages
ms.assetid: 60b3326e-e7e2-4729-95fc-b682e7ad5c99
author: acangialosi
ms.author: anthc
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 16f96191115a509e07b5263f1d10d53ea3b2cc9c
ms.sourcegitcommit: 4ae5e9817ad13edd05425febb322b5be6d3c3425
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/11/2020
ms.locfileid: "90037037"
---
# <a name="determine-whether-to-implement-a-source-control-vspackage"></a>确定是否实现源代码管理 VSPackage

本部分然后详细阐述源代码管理插件和源代码管理 Vspackage 的选择，用于扩展源代码管理解决方案，并提供有关选择合适的集成路径的广义指导。

## <a name="small-source-control-solution-with-limited-resources"></a>资源有限的小型源代码管理解决方案

 如果资源有限，而且不能承受写入源代码管理包的开销，则可以创建基于源代码管理插件的插件。这样做使您可以与源代码管理包并行工作，并且您可以根据需要在源代码管理插件和包之间进行切换。 有关详细信息，请参阅 [注册和选择](../../extensibility/internals/registration-and-selection-source-control-vspackage.md)。

## <a name="large-source-control-solution-with-a-rich-feature-set"></a>具有丰富功能集的大型源代码管理解决方案

 如果要实现一个源代码管理解决方案，该解决方案提供一个使用源代码管理插件 API 未充分捕获的丰富源代码管理模型，则可以将源代码管理包视为集成路径。 这尤其适用于替换源代码管理适配器包 (它与源代码管理插件通信，并提供自己的基本源代码管理 UI) ，以便能够以自定义方式处理源代码管理事件。 如果你已经有一个令人满意的源代码管理 UI，并且想要在中保留该体验 [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] ，则源代码管理包选项仅允许你这样做。 源代码管理包不是泛型包，而是专门为与 IDE 一起使用而设计的 [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] 。

 如果要实现一个源代码管理解决方案，该解决方案可为源代码管理逻辑和 UI 提供灵活性和更丰富的控制，您可能更倾向于源代码管理包集成路由。 你可以：

1. 注册自己的源代码管理 VSPackage (参阅 [注册和选择](../../extensibility/internals/registration-and-selection-source-control-vspackage.md)) 。

2. 将默认源代码管理 UI 替换为自定义 UI (参阅 [自定义用户界面](../../extensibility/internals/custom-user-interface-source-control-vspackage.md)) 。

3. 指定要使用的标志符号并处理解决方案资源管理器标志符号事件 (请参阅 [标志符号控件](../../extensibility/internals/glyph-control-source-control-vspackage.md)) 。

4. 处理查询编辑和查询保存事件 (参阅 [查询编辑查询保存](../../extensibility/internals/query-edit-query-save-source-control-vspackage.md)) 。

## <a name="see-also"></a>另请参阅

- [创建源代码管理插件](../../extensibility/internals/creating-a-source-control-plug-in.md)
