---
title: "-ZW (Windows Runtime Compilation) | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology:  
  - "cpp-tools"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "VC.Project.VCCLCompilerTool.CompileAsWinRT"
  - "/zw"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "/ZW"
  - "-ZW compiler option"
  - "/ZW compiler option"
  - "-ZW"
  - "Windows Runtime compiler option"
ms.assetid: 0fe362b0-9526-498b-96e0-00d7a965a248
caps.latest.revision: 13
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
translation.priority.ht: 
  - "cs-cz"
  - "de-de"
  - "es-es"
  - "fr-fr"
  - "it-it"
  - "ja-jp"
  - "ko-kr"
  - "pl-pl"
  - "pt-br"
  - "ru-ru"
  - "tr-tr"
  - "zh-cn"
  - "zh-tw"
---
# /ZW (Windows Runtime Compilation)
Compiles source code to support [!INCLUDE[cppwrt](../../build/reference/includes/cppwrt_md.md)] ([!INCLUDE[cppwrt_short](../../build/reference/includes/cppwrt_short_md.md)]) for the creation of [!INCLUDE[win8_appname_long](../../build/includes/win8_appname_long_md.md)] apps.  
  
 When you use **/ZW** to compile, always specify **/EHsc** as well.  
  
## Syntax  
  
```cpp  
/ZW /EHsc  
/ZW:nostdlib /EHsc  
```  
  
## Arguments  
 nostdlib  
 Indicates that Platform.winmd, Windows.Foundation.winmd, and other default Windows metadata (.winmd) files are not automatically included in the compilation. Instead, you must use the [/FU (Name Forced #using File)](../../build/reference/fu-name-forced-hash-using-file.md) compiler option to explicitly specify Windows metadata files.  
  
## Remarks  
 When you specify the **/ZW** option, the compiler supports these features:  
  
-   The required metadata files, namespaces, data types, and functions that your app requires to execute in the Windows Runtime.  
  
-   Automatic reference-counting of Windows Runtime objects, and automatic discarding of an object when its reference count goes to zero.  
  
 Because the incremental linker does not support the Windows metadata included in .obj files by using the **/ZW** option, the [/Gm (Enable Minimal Rebuild)](../../build/reference/gm-enable-minimal-rebuild.md) option is incompatible with **/ZW**.  
  
 For more information, see [Visual C++ Language Reference](../../cppcx/visual-c-language-reference-c-cx.md).  
  
## Requirements  
  
## See Also  
 [Compiler Options](../../build/reference/compiler-options.md)   
 [Setting Compiler Options](../../build/reference/setting-compiler-options.md)