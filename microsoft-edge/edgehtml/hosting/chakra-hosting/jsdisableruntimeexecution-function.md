---
description: Suspende a execução do script e encerra todos os scripts em execução em um tempo de execução.
title: Função JsDisableRuntimeExecution | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsDisableRuntimeExecution
helpviewer_keywords:
- JsDisableRuntimeExecution function
ms.assetid: 4bd4670a-a9da-4f8c-b3fd-1fd366d915c3
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 6a08e6a7f89c724f8cf1a73afd97d2cb23c0334e
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231625"
---
# Função JsDisableRuntimeExecution

Suspende a execução do script e encerra todos os scripts em execução em um tempo de execução.  
  
## Sintaxe  
  
```cpp  
STDAPI_(JsErrorCode) JsDisableRuntimeExecution(  
   _In_ JsRuntimeHandle runtime  
);  
```  
  
#### Parâmetros  
 `runtime`  
 O tempo de execução a ser suspenso.  
  
## Valor de retorno  
 O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.  
  
## Comentários  
 As chamadas para um tempo de execução suspenso falharão até `JsEnableRuntimeExecution` serem chamadas.  
  
 Essa API não precisa ser chamada no thread em que o tempo de execução está ativado. Embora o tempo de execução seja definido em um estado suspenso, um script em execução pode não ser suspenso imediatamente; um script em execução será encerrado com uma exceção uncatchável o mais rápido possível.  
  
 Suspender a execução em um tempo de execução que já está suspenso não é op.  
  
## Requisitos  
 **Header:** jsrt. h  
  
## Consulte também  
 [Referência (Runtime do JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
