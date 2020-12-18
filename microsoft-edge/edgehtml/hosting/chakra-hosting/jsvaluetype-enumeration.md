---
description: O tipo de JavaScript de um JsValueRef.
title: Enumeração JsValueType | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsValueType
helpviewer_keywords:
- JsValueType enumeration
ms.assetid: 6645e723-e554-41fc-b622-ab54ee044b3d
caps.latest.revision: 16
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 840afcde86d4df80490d463921a74c73e42ddfc2
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231572"
---
# Enumeração JsValueType

O tipo de JavaScript de um JsValueRef.  
  
## Sintaxe  
  
```cpp  
enum JsValueType {  
    JsUndefined      = 0,  
    JsNull           = 1,  
    JsNumber         = 2,  
    JsString         = 3,  
    JsBoolean        = 4,  
    JsObject         = 5,  
    JsFunction       = 6,  
    JsError          = 7,  
    JsArray          = 8,  
    JsSymbol         = 9,  
    JsArrayBuffer    = 10,  
    JsTypedArray     = 11,  
    JsDataView       = 12,  
};  
```  
  
## Parte  
  
### Valores  
  
|Nome|Descrição|  
|----------|-----------------|  
|`JsUndefined`|O valor é o `undefined` valor.|  
|`JsNull`|O valor é o `null` valor.|  
|`JsNumber`|O valor é um valor de número JavaScript.|  
|`JsString`|O valor é um valor de cadeia de caracteres JavaScript.|  
|`JsBoolean`|O valor é um valor booliano de JavaScript.|  
|`JsObject`|O valor é um valor de objeto JavaScript.|  
|`JsFunction`|O valor é um valor de objeto function JavaScript.|  
|`JsError`|O valor é um valor de objeto de erro JavaScript.|  
|`JsArray`|O valor é um valor de objeto de matriz JavaScript.|  
|`JsSymbol`|O valor é um valor de símbolo JavaScript.<br /><br /> Esse valor de enumeração só tem suporte no modo Microsoft Edge.|  
|`JsArrayBuffer`|O valor é um `ArrayBuffer` valor de objeto JavaScript.<br /><br /> Esse valor de enumeração só tem suporte no modo Microsoft Edge.|  
|`JsTypedArray`|O valor é um valor de objeto matriz tipada do JavaScript.<br /><br /> Esse valor de enumeração só tem suporte no modo Microsoft Edge.|  
|`JsDataView`|O valor é um `DataView` valor de objeto JavaScript.<br /><br /> Esse valor de enumeração só tem suporte no modo Microsoft Edge.|  
  
## Requisitos  
 **Header:** jsrt. h  
  
## Consulte também  
 [Referência (Runtime do JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
