---
description: Obtém o limite de memória atual para um tempo de execução.
title: Função JsGetRuntimeMemoryLimit | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsGetRuntimeMemoryLimit
helpviewer_keywords:
- JsGetRuntimeMemoryLimit function
ms.assetid: ed81ca60-99fd-46b0-89ae-f6ac07926904
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: ed04a0fb921d22eea17eaf86ef7a0152fbf2a1d0
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231934"
---
# Função JsGetRuntimeMemoryLimit

Obtém o limite de memória atual para um tempo de execução.  
  
## Sintaxe  
  
```cpp  
STDAPI_(JsErrorCode) JsGetRuntimeMemoryLimit(  
   _In_ JsRuntimeHandle runtime,  
   _Out_ size_t *memoryLimit  
);  
```  
  
#### Parâmetros  
 `runtime`  
 O tempo de execução cujo limite de memória deve ser recuperado.  
  
 `memoryLimit`  
 O limite de memória atual do tempo de execução, em bytes ou-1, se nenhum limite tiver sido definido.  
  
## Valor de retorno  
 O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.  
  
## Comentários  
 O limite de memória de um tempo de execução pode ser sempre recuperado, independentemente do tempo de execução estar ativo ou não em outro thread.  
  
## Requisitos  
 **Header:** jsrt. h  
  
## Consulte também  
 [Referência (Runtime do JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
