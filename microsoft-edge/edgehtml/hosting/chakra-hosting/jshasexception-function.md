---
description: Determina se o tempo de execução do contexto atual está em um estado de exceção.
title: Função JsHasException | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsHasException
helpviewer_keywords:
- JsHasException function
ms.assetid: ac7da3ce-c746-4154-bbb8-bcb0859a8d5b
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 4f4abbd6c69a6b2b6414dae2f1de3a2acf21cc32
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231289"
---
# Função JsHasException

Determina se o tempo de execução do contexto atual está em um estado de exceção.  
  
## Sintaxe  
  
```cpp  
STDAPI_(JsErrorCode) JsHasException(  
   _Out_ bool *hasException  
);  
```  
  
#### Parâmetros  
 `hasException`  
 Se o tempo de execução do contexto atual está no estado de exceção.  
  
## Valor de retorno  
 O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.  
  
## Comentários  
 Se uma chamada no tempo de execução resulta em uma exceção (como resultado da execução de um script ou devido a uma falha de conversão), o tempo de execução é colocado em um "estado de exceção". Todas as chamadas em qualquer contexto criado pelo tempo de execução (exceto para APIs de exceção) falharão `JsErrorInExceptionState` até que a exceção seja desmarcada.  
  
 Se o tempo de execução do contexto atual estiver no estado de exceção quando um retorno de chamada retornar ao mecanismo, o mecanismo relançará automaticamente a exceção.  
  
 Requer um contexto de script ativo.  
  
## Requisitos  
 **Header:** jsrt. h  
  
## Consulte também  
 [Referência (Runtime do JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
