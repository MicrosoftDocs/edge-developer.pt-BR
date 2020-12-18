---
description: Obtém o uso de memória atual para um tempo de execução.
title: Função JsGetRuntimeMemoryUsage | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsGetRuntimeMemoryUsage
helpviewer_keywords:
- JsGetRuntimeMemoryUsage function
ms.assetid: b9bd4146-bfbc-4cb1-a0e9-a0ded7fb09bd
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: a9c8d59e8cf73ad178f539f2f9f0ed191ceb47fd
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231995"
---
# Função JsGetRuntimeMemoryUsage

Obtém o uso de memória atual para um tempo de execução.  
  
## Sintaxe  
  
```cpp  
STDAPI_(JsErrorCode) JsGetRuntimeMemoryUsage(  
   _In_ JsRuntimeHandle runtime,  
   _Out_ size_t *memoryUsage  
);  
```  
  
#### Parâmetros  
 `runtime`  
 O tempo de execução cujo uso da memória deve ser recuperado.  
  
 `memoryUsage`  
 O uso atual da memória do tempo de execução, em bytes.  
  
## Valor de retorno  
 O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.  
  
## Comentários  
 O uso da memória pode sempre ser recuperado, independentemente do tempo de execução estar ativo ou não em outro thread.  
  
## Requisitos  
 **Header:** jsrt. h  
  
## Consulte também  
 [Referência (Runtime do JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
