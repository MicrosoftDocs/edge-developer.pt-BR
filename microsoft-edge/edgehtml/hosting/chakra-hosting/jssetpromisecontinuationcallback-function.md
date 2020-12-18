---
description: Define uma função de retorno de chamada de continuação Promise que é chamada pelo contexto quando uma tarefa precisa ser colocada em fila para execução futura.
title: Função JsSetPromiseContinuationCallback | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 6ef0faf4-1500-4bd9-aeca-c208492af8ea
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: da928431f05831c95d5bc116dbd129de9cb5f3b4
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231660"
---
# Função JsSetPromiseContinuationCallback

Define uma função de retorno de chamada de continuação Promise que é chamada pelo contexto quando uma tarefa precisa ser colocada em fila para execução futura.  
  
## Sintaxe  
  
```cpp  
STDAPI_(JsErrorCode) JsSetPromiseContinuationCallback(  
   _In_ JsPromiseContinuationCallback promiseContinuationCallback,  
   _In_opt_ void *callbackState  
);  
```  
  
#### Parâmetros  
 `promiseContinuationCallback`  
 A função de retorno de chamada sendo definida.  
  
 `callbackState`  
 Estado fornecido pelo usuário que será devolvido ao retorno de chamada.  
  
## Valor de retorno  
 O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.  
  
## Comentários  
 Requer um contexto de script ativo.  
  
 Essa API só tem suporte no modo EdgeHTML.  
  
## Requisitos  
 **Header:** jsrt. h  
  
## Consulte também  
 [Referência (Runtime do JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
