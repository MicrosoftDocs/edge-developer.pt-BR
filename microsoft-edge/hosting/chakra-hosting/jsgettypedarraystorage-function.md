---
description: Obtém o armazenamento de memória subjacente usado por uma matriz digitada.
title: Função JsGetTypedArrayStorage | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 52e4ac5f-cc71-456d-95de-a48f7327503d
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: f03414d64fa819ac464217c8362d02e866d45296
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10562176"
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
 [Referência (tempo de execução JavaScript)](../chakra-hosting/reference-javascript-runtime.md)