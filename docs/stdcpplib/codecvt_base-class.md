---
title: "codecvt_base Class"
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
  - "codecvt_base"
  - "xlocale/std::codecvt_base"
  - "std.codecvt_base"
  - "std::codecvt_base"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "codecvt_base class"
ms.assetid: 7e95c083-91b4-4b3f-8918-0d4ea244a040
caps.latest.revision: 19
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
# codecvt_base Class
A base class for the codecvt class that is used to define an enumeration type referred to as **result**, used as the return type for the facet member functions to indicate the result of a conversion.  
  
## Syntax  
  
```
class codecvt_base : public locale::facet {
public:
    enum result {ok,
    partial,
    error,
    noconv};
    codecvt_base(
 size_t _Refs = 0);

    bool always_noconv() const;

    int max_length() const;

    int encoding() const;

 ~codecvt_base()
protected:
    virtual bool do_always_noconv() const;

    virtual int do_max_length() const;

    virtual int do_encoding() const;

};
```  
  
## Remarks  
 The class describes an enumeration common to all specializations of template class [codecvt](../stdcpplib/codecvt-class.md). The enumeration result describes the possible return values from [do_in](../stdcpplib/codecvt-class.md#codecvt__do_in) or [do_out](../stdcpplib/codecvt-class.md#codecvt__do_out):  
  
- **ok** if the conversion between internal and external character encodings succeeds.  
  
- **partial** if the destination is not large enough for the conversion to succeed.  
  
- **error** if the source sequence is ill formed.  
  
- **noconv** if the function performs no conversion.  
  
## Requirements  
 **Header:** \<locale>  
  
 **Namespace:** std  
  
## See Also  
 [Thread Safety in the C++ Standard Library](../stdcpplib/thread-safety-in-the-c---standard-library.md)
