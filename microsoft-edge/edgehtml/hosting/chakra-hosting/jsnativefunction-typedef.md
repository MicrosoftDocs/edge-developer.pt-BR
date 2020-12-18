---
description: Um retorno de chamada de função.
title: Typedef JsNativeFunction | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 56ef6cdf-4ca9-4f7c-b953-e661addb1a8e
caps.latest.revision: 5
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 891fe55f776e8519a5d3c187104b2bc326336482
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231245"
---
# Typedef JsNativeFunction 

Um retorno de chamada de função.  
  
## Sintaxe  
  
```cpp  
typedef _Ret_maybenull_ JsValueRef (CALLBACK * JsNativeFunction)(  
   _In_ JsValueRef callee,  
   _In_ bool isConstructCall,  
   _In_ JsValueRef *arguments,  
   _In_ unsigned short argumentCount  
);  
```  
  
#### Parâmetros  
 destinatário  
 Um `Function` objeto que representa a função que está sendo invocada.  
  
 isConstructCall  
 Indica se esta é uma chamada regular ou ' nova '.  
  
 arguments  
 Os argumentos para a chamada.  
  
 argumentCount  
 O número de argumentos.  
  
## Valor da propriedade/valor de retorno  
 O resultado da chamada, se houver.  
  
## Requisitos  
 **Header:** jsrt. h  
  
## Consulte também  
 [Referência (Runtime do JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
