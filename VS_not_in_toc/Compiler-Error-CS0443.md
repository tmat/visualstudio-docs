---
title: "Compiler Error CS0443"
ms.custom: na
ms.date: 10/01/2016
ms.devlang: 
  - CSharp
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 8f7f71ff-5eb5-4a1d-80ff-77303472eb8e
caps.latest.revision: 10
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
# Compiler Error CS0443
Syntax error, value expected  
  
 This error occurs when you reference an array without specifying a value for the array index.  
  
## Example  
 The following code generates CS0443.  
  
```  
// CS0443.cs   
using System;   
class MyClass   
{  
    public static void Main()      
    {  
        int[,] x = new int[1,5];  
        if (x[] == 5) {} // CS0443  
        // if (x[0, 0] == 5) {}   
    }  
}  
```