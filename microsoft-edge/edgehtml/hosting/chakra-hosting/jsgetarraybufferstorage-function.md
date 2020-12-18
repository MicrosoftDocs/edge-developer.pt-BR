---
description: Obtém o armazenamento de memória subjacente usado por um ArrayBuffer.
title: Função JsGetArrayBufferStorage | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 712ae298-36a9-47ef-b089-e51835c056bc
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 64b031a81506e68322759eff49da7467cac6f219
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231549"
---
# Função JsGetArrayBufferStorage

Obtém o armazenamento de memória subjacente usado por um `ArrayBuffer` .  
  
## Sintaxe  
  
```cpp  
JsErrorCode STDAPI_ JsGetArrayBufferStorage(  
   _In_ JsValueRef arrayBuffer,  
   _Outptr_result_bytebuffer_(*bufferLength) BYTE **buffer,  
   _Out_ unsigned int *bufferLength  
);  
```  
  
#### Parâmetros  
 `arrayBuffer`  
 A instância ArrayBuffer.  
  
 `buffer`  
 O buffer do ArrayBuffer. O tempo de vida do buffer retornado é o mesmo que o tempo de vida do `ArrayBuffer` . O ponteiro de buffer não conta como uma referência para a `ArrayBuffer` finalidade da coleta de lixo.  
  
 `bufferLength`  
 O número de bytes no buffer.  
  
## Valor de retorno  
 O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.  
  
## Comentários  
 Requer um contexto de script ativo.  
  
 Essa API só tem suporte no modo Microsoft Edge.  
  
## Requisitos  
 **Header:** jsrt. h  
  
## Consulte também  
 [Referência (Runtime do JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
