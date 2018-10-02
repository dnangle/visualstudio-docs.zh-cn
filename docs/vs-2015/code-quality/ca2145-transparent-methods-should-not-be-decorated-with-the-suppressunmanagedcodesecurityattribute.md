---
title: CA2145： 透明方法不应修饰使用 SuppressUnmanagedCodeSecurityAttribute |Microsoft Docs
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-devops-test
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- CA2145
ms.assetid: 81970700-b438-4b3b-9239-16887e16f7b7
caps.latest.revision: 13
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: 7dcb7d2596a03bc78eed7dc4c3a1455c91478b04
ms.sourcegitcommit: 568bb0b944d16cfe1af624879fa3d3594d020187
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/13/2018
ms.locfileid: "47588954"
---
# <a name="ca2145-transparent-methods-should-not-be-decorated-with-the-suppressunmanagedcodesecurityattribute"></a>CA2145：不应使用 SuppressUnmanagedCodeSecurityAttribute 修饰透明方法
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

本主题的最新版本，请参阅[CA2145： 不应使用 SuppressUnmanagedCodeSecurityAttribute 修饰透明方法](https://docs.microsoft.com/visualstudio/code-quality/ca2145-transparent-methods-should-not-be-decorated-with-the-suppressunmanagedcodesecurityattribute)。

|||
|-|-|
|TypeName|TransparentMethodsShouldNotUseSuppressUnmanagedCodeSecurity|
|CheckId|CA2145|
|类别|Microsoft.Security|
|是否重大更改|重大|

## <a name="cause"></a>原因
 透明方法，使用标记的方法<xref:System.Security.SecuritySafeCriticalAttribute>方法或包含一种方法的类型将标有<xref:System.Security.SuppressUnmanagedCodeSecurityAttribute>属性。

## <a name="rule-description"></a>规则说明
 使用修饰方法<xref:System.Security.SuppressUnmanagedCodeSecurityAttribute>属性具有调用它的任何方法隐式的 LinkDemand。 此 LinkDemand 要求调用代码是关键安全的。 标记使用 SuppressUnmanagedCodeSecurity 的方法<xref:System.Security.SecurityCriticalAttribute>属性会使此需求更明显的方法的调用方。

## <a name="how-to-fix-violations"></a>如何解决冲突
 若要解决此规则的冲突，标记该方法或类型具有<xref:System.Security.SecurityCriticalAttribute>属性。

## <a name="when-to-suppress-warnings"></a>何时禁止显示警告
 不禁止显示此规则发出的警告。

### <a name="code"></a>代码
 [!code-csharp[FxCop.Security.CA2145.TransparentMethodsShouldNotUseSuppressUnmanagedCodeSecurity#1](../snippets/csharp/VS_Snippets_CodeAnalysis/fxcop.security.ca2145.transparentmethodsshouldnotusesuppressunmanagedcodesecurity/cs/ca2145.cs#1)]

### <a name="comments"></a>注释


