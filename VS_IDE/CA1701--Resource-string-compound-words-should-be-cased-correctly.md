---
title: "CA1701: Resource string compound words should be cased correctly"
ms.custom: na
ms.date: 10/03/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-devops-test
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 4ddbe09f-24b8-4c47-9373-a06f4487ca0d
caps.latest.revision: 24
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
# CA1701: Resource string compound words should be cased correctly
|||  
|-|-|  
|TypeName|ResourceStringCompoundWordsShouldBeCasedCorrectly|  
|CheckId|CA1701|  
|Category|Microsoft.Naming|  
|Breaking Change|Non-breaking|  
  
## Cause  
 A resource string contains a compound word that does not appear to be cased correctly.  
  
## Rule Description  
 Each word in the resource string is split into tokens that are based on the casing. Each contiguous two-token combination is checked by the Microsoft spelling checker library. If recognized, the word produces a violation of the rule. Examples of compound words that cause a violation are "CheckSum" and "MultiPart", which should be cased as "Checksum" and "Multipart", respectively. Due to previous common usage, several exceptions are built into the rule, and several single words are flagged, such as "Toolbar" and "Filename", that should be cased as two distinct words. In this example, "ToolBar" and "FileName" would be flagged.  
  
 Naming conventions provide a common look for libraries that target the common language runtime. This reduces the learning curve that is required for new software libraries, and increases customer confidence that the library was developed by someone who has expertise in developing managed code.  
  
## How to Fix Violations  
 Change the word so that it is cased correctly.  
  
## When to Suppress Warnings  
 It is safe to suppress a warning from this rule if both parts of the compound word are recognized by the spelling dictionary and the intent is to use two words.  
  
 You can also add compound words to a custom dictionary for the spelling checker. Words in the custom dictionary do not cause violations. For more information, see [How to: Customize the Code Analysis Dictionary](../VS_IDE/How-to--Customize-the-Code-Analysis-Dictionary.md).  
  
## Related Rules  
 [CA1702: Compound words should be cased correctly](../VS_IDE/CA1702--Compound-words-should-be-cased-correctly.md)  
  
 [CA1709: Identifiers should be cased correctly](../VS_IDE/CA1709--Identifiers-should-be-cased-correctly.md)  
  
 [CA1708: Identifiers should differ by more than case](../VS_IDE/CA1708--Identifiers-should-differ-by-more-than-case.md)  
  
## See Also  
 [Capitalization Conventions](../Topic/Capitalization%20Conventions.md)   
 [Naming Guidelines](../Topic/Naming%20Guidelines.md)