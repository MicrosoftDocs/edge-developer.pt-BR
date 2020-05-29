---
description: Define o retorno de chamada a ser usado para invocar uma conclusão de projeção para o thread dos chamadores obrigatórios.
title: Função JsSetProjectionEnqueueCallback | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: c751ccef-20d2-4d41-9568-1c54adf47cdf
caps.latest.revision: 4
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 02da0238360b0dc6fff9bb86c9f5ab04d1ba7112
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10562101"
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
 [Referência (tempo de execução JavaScript)](../chakra-hosting/reference-javascript-runtime.md)