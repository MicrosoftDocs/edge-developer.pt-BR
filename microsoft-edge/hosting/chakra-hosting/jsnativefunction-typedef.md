---
description: Um retorno de chamada de função.
title: Typedef JsNativeFunction | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 56ef6cdf-4ca9-4f7c-b953-e661addb1a8e
caps.latest.revision: 5
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: c0b73a11d3a0b2ed0867ef001f3c29c5643132a0
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561019"
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
 [Referência (tempo de execução JavaScript)](../chakra-hosting/reference-javascript-runtime.md)