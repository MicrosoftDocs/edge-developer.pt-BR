---
description: Obtém o armazenamento de memória subjacente usado por um ArrayBuffer.
title: Função JsGetArrayBufferStorage | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 712ae298-36a9-47ef-b089-e51835c056bc
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 1e8d265f3e81015ba9f5d0547b6b1c7246c23ce5
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10562196"
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
 [Referência (tempo de execução JavaScript)](../chakra-hosting/reference-javascript-runtime.md)