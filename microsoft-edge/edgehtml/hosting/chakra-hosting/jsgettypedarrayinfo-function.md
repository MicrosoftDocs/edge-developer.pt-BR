---
description: Obtém propriedades usadas com frequência de uma matriz digitada.
title: Função JsGetTypedArrayInfo | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 992bc4e9-3d06-4ad2-8b6b-88a437360f81
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: fdc9a05a2aebdabfd0c8e95c848d3bd5f97e580a
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231789"
---
# Função JsGetTypedArrayInfo

Obtém propriedades usadas com frequência de uma matriz digitada.  
  
## Sintaxe  
  
```cpp  
STDAPI_(JsErrorCode) JsGetTypedArrayInfo(  
  _In_ JsValueRef typedArray,  
  _Out_opt_ JsTypedArrayType *arrayType,  
  _Out_opt_ JsValueRef *arrayBuffer,  
  _Out_opt_ unsigned int *byteOffset,  
  _Out_opt_ unsigned int *byteLength  
);  
  
```  
  
#### Parâmetros  
 `typedArray`  
 A instância de matriz tipada.  
  
 `arrayType`  
 O tipo da matriz.  
  
 `arrayBuffer`  
 A `ArrayBuffer` BACKSTORE da matriz.  
  
 `byteOffset`  
 O offset em bytes do início de arrayBuffer referenciado pela matriz.  
  
 `byteLength`  
 O número de bytes na matriz.  
  
## Valor de retorno  
 O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.  
  
## Comentários  
 Requer um contexto de script ativo.  
  
## Requisitos  
 **Header:** jsrt. h  
  
## Consulte também  
 [Referência (Runtime do JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
