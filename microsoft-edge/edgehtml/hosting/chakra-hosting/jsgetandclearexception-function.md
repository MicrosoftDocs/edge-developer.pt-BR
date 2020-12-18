---
description: Retorna a exceção que causou o tempo de execução do contexto atual para estar no estado de exceção e redefine o estado de exceção desse tempo de execução.
title: Função JsGetAndClearException | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsGetAndClearException
helpviewer_keywords:
- JsGetAndClearException function
ms.assetid: 6aec8a88-41ee-47f6-b5f4-32f3cae6bb7b
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: cb296ea351d0466a856d5ac020550ebacc254ac9
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231548"
---
# Função JsGetAndClearException

Retorna a exceção que causou o tempo de execução do contexto atual para estar no estado de exceção e redefine o estado de exceção desse tempo de execução.  
  
## Sintaxe  
  
```cpp  
STDAPI_(JsErrorCode) JsGetAndClearException(  
   _Out_ JsValueRef *exception  
);  
```  
  
#### Parâmetros  
 `exception`  
 A exceção para o tempo de execução do contexto atual.  
  
## Valor de retorno  
 O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.  
  
## Comentários  
 Se o tempo de execução do contexto atual não estiver em um estado de exceção, essa API retornará `JsErrorInvalidArgument` . Se o tempo de execução estiver desabilitado, isso retornará uma exceção indicando que o script foi encerrado, mas não limpará a exceção (a exceção será desmarcada se o tempo de execução for habilitado novamente usando `JsEnableRuntimeExecution` ).  
  
 Requer um contexto de script ativo.  
  
## Requisitos  
 **Header:** jsrt. h  
  
## Consulte também  
 [Referência (Runtime do JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
