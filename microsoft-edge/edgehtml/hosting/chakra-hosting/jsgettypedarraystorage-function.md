---
description: Obtém o armazenamento de memória subjacente usado por uma matriz digitada.
title: Função JsGetTypedArrayStorage | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 52e4ac5f-cc71-456d-95de-a48f7327503d
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 442727228433368de14bac528ea416fcc2a95fa8
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231286"
---
# Função JsGetTypedArrayStorage

Obtém o armazenamento de memória subjacente usado por uma matriz digitada.  
  
## Sintaxe  
  
```cpp  
STDAPI_(JsErrorCode) JsGetTypedArrayStorage(  
   _In_ JsValueRef typedArray,  
   _Outptr_result_bytebuffer_(*bufferLength) BYTE **buffer,  
   _Out_ unsigned int *bufferLength,  
   _Out_opt_ JsTypedArrayType *arrayType,  
   _Out_opt_ int *elementSize  
);  
```  
  
#### Parâmetros  
 `typedArray`  
 A instância de matriz tipada.  
  
 `buffer`  
 O buffer da matriz. O tempo de vida do buffer retornado é o mesmo que o tempo de vida da matriz. O ponteiro de buffer não conta como uma referência à matriz para a finalidade da coleta de lixo.  
  
 `bufferLength`  
 O número de bytes no buffer.  
  
 `arrayType`  
 O tipo da matriz.  
  
 `elementSize`  
 O tamanho de um elemento da matriz.  
  
## Valor de retorno  
 O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.  
  
## Comentários  
 Requer um contexto de script ativo.  
  
 Essa API só tem suporte no modo Microsoft Edge.  
  
## Requisitos  
 **Header:** jsrt. h  
  
## Consulte também  
 [Referência (Runtime do JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
