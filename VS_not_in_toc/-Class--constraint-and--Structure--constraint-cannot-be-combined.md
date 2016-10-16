---
title: "&#39;Class&#39; constraint and &#39;Structure&#39; constraint cannot be combined"
ms.custom: na
ms.date: 10/01/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: f41a581b-afca-4173-bc82-b35ed49caba0
caps.latest.revision: 7
manager: douge
translation.priority.ht: 
  - de-de
  - es-es
  - fr-fr
  - it-it
  - ja-jp
  - ko-kr
  - ru-ru
  - zh-cn
  - zh-tw
translation.priority.mt: 
  - cs-cz
  - pl-pl
  - pt-br
  - tr-tr
---
# &#39;Class&#39; constraint and &#39;Structure&#39; constraint cannot be combined
A constraint list includes both the [Class (Visual Basic)](assetId:///0777c6e6-46bc-451b-ad70-57b49d4ef4f7) constraint and the [Structure (Visual Basic)](assetId:///263ce115-ac36-4c05-8cb7-0e0eead5c6d0) constraint.  
  
 A constraint list on a type parameter can specify that the type argument passed to that type parameter must be a value type (with the `Structure` constraint) or must be a reference type (with the `Class` constraint). You cannot specify both constraints on the same type parameter, and you cannot specify either one more than once.  
  
 **Error ID:** BC32104  
  
### To correct this error  
  
1.  Decide whether you want to require a value type or a reference type for the type argument.  
  
    -   If you want the type argument to be a value type, remove the `Class` keyword from the constraint list.  
  
    -   If you want the type argument to be a reference type, remove the `Structure` keyword from the constraint list.  
  
## See Also  
 [Generic Types in Visual Basic](../Topic/Generic%20Types%20in%20Visual%20Basic%20\(Visual%20Basic\).md)   
 [Value Types and Reference Types](../Topic/Value%20Types%20and%20Reference%20Types.md)