---
description: Suspende a execução do script e encerra todos os scripts em execução em um tempo de execução.
title: Função JsDisableRuntimeExecution | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsDisableRuntimeExecution
helpviewer_keywords:
- JsDisableRuntimeExecution function
ms.assetid: 4bd4670a-a9da-4f8c-b3fd-1fd366d915c3
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 575947d3038eaa136e9d6ae62507501bc768eabe
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561071"
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
 [Referência (tempo de execução JavaScript)](../chakra-hosting/reference-javascript-runtime.md)