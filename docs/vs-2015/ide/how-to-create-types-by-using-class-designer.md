---
title: 如何：使用类设计器创建类型 | Microsoft Docs
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-general
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- VS.Clr.ClrAttributesDialog
helpviewer_keywords:
- custom attributes, applying
- class diagrams, creating types
- classes [Visual Studio], creating with Class Designer
- Class Designer [Visual Studio], creating classes
- types [Visual Studio], class diagrams
- attributes [Visual Studio], applying custom
ms.assetid: 94458c31-28bc-40e2-9737-85868788a0e5
caps.latest.revision: 45
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: f7671b1336b0b722f02cc100c7055fef817cb582
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/22/2018
ms.locfileid: "47483178"
---
# <a name="how-to-create-types-by-using-class-designer"></a>如何：使用类设计器创建类型
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

本主题的最新版本，请参阅[如何： 使用类设计器创建类型](https://docs.microsoft.com/visualstudio/ide/how-to-create-types-by-using-class-designer)。  
  
若要设计 Visual C# .NET 和 Visual Basic .NET 项目的新类型，则在类图上创建它们。 若要查看现有类型，请参阅[如何：查看现有类型（类设计器）](../ide/how-to-view-existing-types-class-designer.md)。  
  
-   [创建新类型](#CreateType)  
  
-   [将自定义特性应用于类型](#CustAttributeType)  
  
-   [将自定义特性应用于类型成员](#CustAttributeMember)  
  
##  <a name="CreateType"></a>创建新类型  
  
1.  在“工具箱”的“类设计器”下，将以下之一拖动到类图上：  
  
    -   “类”或“抽象类”  
  
    -   **Enum**  
  
    -   **Interface**  
  
    -   “结构”(VB) 或“结构”(C#)  
  
    -   **Delegate**  
  
    -   “模块”（仅限 VB）  
  
2.  为该类型命名。 然后选择其访问级别。  
  
3.  选择要在其中添加该类型的初始代码的文件：  
  
    -   若要创建新文件并将其添加到当前项目，请选择“创建新文件”，并为该文件命名。  
  
    -   若要将代码添加到现有文件，请选择“添加到现有文件”。  
  
         如果你的解决方案有共享跨多个应用的代码的项目，你可以将新类型添加到应用项目中的类图，但前提是相应的类文件在同一应用项目中或共享项目中。  
  
4.  现在添加其他项以定义该类型：  
  
    |||  
    |-|-|  
    |**对于**|**添加**|  
    |类、抽象类、结构|定义类型的方法、属性、字段、事件、构造函数（方法）、析构函数（方法）和常量|  
    |枚举|组成枚举的字段值|  
    |接口|组成接口的方法、属性和事件|  
    |委托|定义委托的参数|  
    |模块|定义模块的方法、属性、字段、事件、构造函数（方法）和常量|  
  
     请参阅[创建成员](../ide/creating-and-configuring-type-members-class-designer.md#CreateMembers)。  
  
##  <a name="CustAttributeType"></a>将自定义特性应用于类型  
  
1.  在类图上单击类型的形状。  
  
2.  在属性窗口中下, 一步**自定义特性**属性对于类型，单击省略号 （...） 按钮。  
  
3.  添加一个或多个自定义特性，一行一个。 请不要将它们放在括号内。  
  
     完毕后，自定义特性随即应用于类型。  
  
##  <a name="CustAttributeMember"></a>将自定义特性应用于类型成员  
  
1.  在类图上类型的形状中单击成员的名称，或者在“类详细信息”窗口中单击成员所在的行。  
  
2.  在“属性”窗口中，查找成员的“自定义特性”属性。  
  
3.  添加一个或多个自定义特性，一行一个。 请不要将它们放在括号内。  
  
     完毕后，自定义特性随即应用于类型。  
  
## <a name="see-also"></a>请参阅  
 [如何：创建类型之间的继承（类设计器）](../ide/how-to-create-inheritance-between-types-class-designer.md)   
 [如何：创建类型之间的关联（类设计器）](../ide/how-to-create-associations-between-types-class-designer.md)   
 [创建和配置类型成员（类设计器）](../ide/creating-and-configuring-type-members-class-designer.md)   
 [使用类图（类设计器）](../ide/working-with-class-diagrams-class-designer.md)   
 [设计类和类型（类设计器）](../ide/designing-classes-and-types-class-designer.md)


