---
description: Define o tempo de execução do contexto atual como um estado de exceção.
title: Função JsSetException | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsSetException
helpviewer_keywords:
- JsSetException function
ms.assetid: c528793a-2e1b-4ee1-bd2e-e63fd547dc40
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 2c2e3840d2a831db23a525c5d8854b9b2fcfb8c9
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231621"
---
# Função JsSetException

Define o tempo de execução do contexto atual como um estado de exceção.  
  
## Sintaxe  
  
```cpp  
STDAPI_(JsErrorCode) JsSetException(  
   _In_ JsValueRef exception  
);  
```  
  
#### Parâmetros  
 `exception`  
 A exceção JavaScript a ser definida para o tempo de execução do contexto atual.  
  
## Valor de retorno  
 `JsNoError` Se o mecanismo tiver sido definido como um estado de exceção, um código de falha também.  
  
## Comentários  
 Se o tempo de execução do contexto atual já estiver em um estado de exceção, essa API retornará `JsErrorInExceptionState` .  
  
 Requer um contexto de script ativo.  
  
## Requisitos  
 **Header:** jsrt. h  
  
## Consulte também  
 [Referência (Runtime do JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
