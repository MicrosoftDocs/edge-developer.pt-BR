---
description: Define o retorno de chamada a ser usado para invocar uma conclusão de projeção para o thread dos chamadores obrigatórios.
title: Função JsSetProjectionEnqueueCallback | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: c751ccef-20d2-4d41-9568-1c54adf47cdf
caps.latest.revision: 4
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 7dfedfeb1df5a97159a211795a2dd072d239bb35
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231405"
---
# Função JsSetProjectionEnqueueCallback

Define o retorno de chamada a ser usado para invocar uma conclusão de projeção para o thread dos chamadores obrigatórios.  
  
## Sintaxe  
  
```cpp  
STDAPI_(JsErrorCode) JsSetProjectionEnqueueCallback(  
   _In_ JsProjectionEnqueueCallback projectionEnqueueCallback,  
   _In_opt_ void *projectionEnqueueContext);  
  
```  
  
#### Parâmetros  
 `projectionEnqueueContext`  
 O retorno de chamada que será invocado sempre que uma conclusão de projeção ocorrer em um thread em segundo plano.  
  
 `callbackState`  
 O contexto do aplicativo fornecido para `projectionEnqueueContext` .  
  
## Valor de retorno  
 O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.  
  
## Comentários  
 Requer um contexto de script ativo.  
  
 A chamada deve ser proveniente de um outro apartment COM ou de um thread diferente no mesmo MTA.  
  
 Essa API só tem suporte no modo EdgeHTML.  
  
> [!CAUTION]
>  No momento, não há suporte para PInvoke para essa API.  
  
## Requisitos  
 **Header:** jsrt. h  
  
## Consulte também  
 [Referência (Runtime do JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
