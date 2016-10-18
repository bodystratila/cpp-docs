---
title: "ISessionPropertiesImpl Class"
ms.custom: na
ms.date: "10/14/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: na
ms.topic: "article"
f1_keywords: 
  - "ISessionPropertiesImpl"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "ISessionPropertiesImpl class"
ms.assetid: ca0ba254-c7dc-4c52-abec-cf895a0c6a63
caps.latest.revision: 9
ms.author: "mblome"
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
# ISessionPropertiesImpl Class
Provides an implementation of the [ISessionProperties](https://msdn.microsoft.com/en-us/library/ms713721.aspx) interface.  
  
## Syntax  
  
```  
template <class T, class PropClass = T>  
class ATL_NO_VTABLE ISessionPropertiesImpl :  
   public ISessionProperties,    
   public CUtlProps<PropClass>  
```  
  
#### Parameters  
 `T`  
 Your class, derived from `ISessionPropertiesImpl`.  
  
 `PropClass`  
 A user-definable property class that defaults to `T`.  
  
## Members  
  
### Interface Methods  
  
|||  
|-|-|  
|[GetProperties](../data/isessionpropertiesimpl--getproperties.md)|Returns the list of properties in the Session property group that are currently set on the session.|  
|[SetProperties](../data/isessionpropertiesimpl--setproperties.md)|Sets properties in the Session property group.|  
  
## Remarks  
 A mandatory interface on sessions. This class implements session properties by calling a static function defined by the [property set map](../data/begin_propset_map.md). The property set map should be specified in your session class.  
  
## Requirements  
 **Header:** atldb.h  
  
## See Also  
 [OLE DB Provider Templates](../data/ole-db-provider-templates--c---.md)   
 [OLE DB Provider Template Architecture](../data/ole-db-provider-template-architecture.md)