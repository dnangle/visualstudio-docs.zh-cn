---
title: 什么&#39;在 Visual Studio 中设计的新增功能的 s |Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-tfs-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-devops-techdebt
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- what's new [VIsual Studio ALM], architecture and modeling
- architecture [Visual Studio Ultimate], modeling
- modeling software [Visual Studio ALM], What's New
ms.assetid: 36ab5c17-6dc0-4075-a28e-a0fa49b11260
caps.latest.revision: 34
author: alexhomer1
ms.author: gewarren
manager: douge
ms.openlocfilehash: 3d6ab30934750f2c825029c1433ea7ca68447dcd
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/12/2018
ms.locfileid: "49204277"
---
# <a name="whats-new-for-design-in-visual-studio"></a>Visual Studio 中用于设计的新增功能
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]
此版本的 Visual Studio 包括以下改进以帮助你更好地理解并设计代码。

 **代码图和依赖项关系图**

 在 Visual Studio Enterprise 中，当你想要了解代码中的特定依赖项时，可通过创建代码图将其可视化。 然后可以使用代码图（在代码旁边显示）导航这些关系。 代码图还可以在你处理或调试代码时，帮助跟踪你在代码中的位置，这样一来，你将在读取更少代码的同时了解关于代码设计的更多信息。

 在最终 (RTM) 版本中，通过将命令组合为与选择、编辑、管理组和更改组内容的布局相关的部分，代码元素和链接的快捷菜单变得更加易于使用。 另请注意，测试项目的显示风格与其他项目不同，并且我们将代码图中的元素图标更新到了更合适的版本。

 ![在新的代码图上显示所选的项](../ide/media/codemapsshowonnewmap.png "CodeMapsShowOnNewMap")

 其他改进包括：

-   **改进的上下关系图**。 对于中型到大型 Visual Studio 解决方案，现在可以使用简化的体系结构菜单来获取更有用的解决方案代码图。 解决方案的程序集按解决方案文件夹进行组合，因此，你可以在上下文中进行查看并利用为结构化解决方案而完成的工作。 你将立即看到项目和程序集引用，然后会显示链接类型。 此外，解决方案外部的程序集以更紧凑的方式进行组合。

-   **测试项目的风格不一样且可以进行筛选**。 现在可以更加轻松快速地在代码图中确定测试项目，因为它们的风格不一样。 还可以将测试项目筛选出来，以便你能够专注于处理应用程序的工作代码。

-   **简化的外部依赖项链接**。 依赖项链接不再表示来自 System.Object、System.ValueType、System.Enum 和 System.Delegate 的继承，这样一来，在代码图中查看外部依赖项变得更加方便。

-   **“深入了解依赖项链接”将筛选器考虑在内**。 展开关系图以了解某个依赖项链接的贡献时，可以获得有用且清晰的关系图。 该关系图不那么杂乱，并将你选择的链接筛选选项考虑在内。

-   **代码元素与其上下文一起添加到代码图**。 因为关系图现在与其上下文一起显示（到可以筛选出来的程序集和解决方案文件夹，如果需要），所以从解决方案资源管理器、类视图、对象浏览器拖放代码元素时，或在解决方案资源管理器中选择元素并选择“在代码图上显示”时，可以获得更加有用的关系图。

-   **更快速地获取反应式代码图**。 拖放操作可以生成即时结果，且节点之间的链接可以更快速地进行创建，而不会影响后续由用户启动的操作，例如展开节点或请求更多节点。 创建代码图而不生成解决方案时，所有极端案例（例如不生成程序集时）现在得到处理。

-   **跳过重新生成你的解决方案。** 在创建和编辑关系图时提供更好的性能。

-   **筛选代码元素节点和组**。 通过根据代码元素的类别显示或隐藏代码元素，以及通过按解决方案文件夹、程序集、命名空间、项目文件夹和类型对代码元素进行组合，可以快速整理代码图。

-   **筛选关系以使关系图更易于阅读**。 链接筛选现在也适用于跨组链接，与早期版本相比，链接筛选让使用筛选器窗口工作时产生的干扰变少。

-   **根据类视图和对象浏览器创建关系图**。 从类视图和对象浏览器窗口将文件和程序集拖放到新的代码图或现有代码图中。

 请参阅 [Map dependencies across your solutions](../modeling/map-dependencies-across-your-solutions.md)。

 **在此版本中其他设计和建模更改：**

-   **层关系图**。 使用类视图和对象浏览器更新这些关系图。 为满足软件设计要求，使用层关系图来描述软件所需的依赖项。 通过查找不满足这些约束条件的代码以及使用此基线验证未来的代码，使代码与此设计保持一致。

-   **UML 关系图**。 不再能够根据代码创建 UML 类图和序列图。 但你仍可使用新的 UML 元素创建这些关系图。

-   **体系结构资源管理器**。 不再能够使用体系结构资源管理器创建关系图。 但你仍可使用解决方案资源管理器。

##  <a name="VersionSupport"></a> 对体系结构和建模工具的版本支持

Visual Studio 2015 现已推出多个版本。 并非所有这些体系结构和建模工具提供支持。 下表显示每个工具的可用性。

|**功能**|**Enterprise**|**Professional**|**Community**|**Express**|
|-----------------|--------------------|----------------------|-------------------|-----------------|
|**代码图**|是|仅支持读取和筛选代码图、 添加新的泛型节点和从所选内容创建新的定向关系图。|-|-|
|**UML 类图**|是|-|-|-|
|**UML 序列图**|是|-|-|-|
|**UML 用例图**|是|-|-|-|
|**UML 活动图**|是|-|-|-|
|**UML 组件图**|是|-|-|-|
|**层关系图**|是|-|-|-|
|**定向关系图**（DGML 关系图）|是|是|-|-|
|**代码克隆**|是|-|-|-|