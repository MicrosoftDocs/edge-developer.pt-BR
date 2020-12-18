---
description: Obtém o armazenamento de memória subjacente usado por um DataView.
title: Função JsGetDataViewStorage | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 7c2180e0-51d5-4cc8-ad21-8bf29ff7c583
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 55f357e4a94b1edbc417ebb14ab99db11083dff4
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231670"
---
# Função JsGetDataViewStorage

Obtém o armazenamento de memória subjacente usado por a `DataView` .  
  
## Sintaxe  
  
```cpp  
STDAPI_(JsErrorCode) JsGetDataViewStorage(  
   _In_ JsValueRef dataView,  
   _Outptr_result_bytebuffer_(*bufferLength) BYTE **buffer,  
   _Out_ unsigned int *bufferLength  
);  
```  
  
#### Parâmetros  
 `dataView`  
 A instância DataView.  
  
 `buffer`  
 O buffer do DataView. O tempo de vida do buffer retornado é o mesmo que o tempo de vida do `DataView` . O ponteiro de buffer não conta como uma referência para a `DataView` finalidade da coleta de lixo.  
  
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
