---
description: Define um retorno de chamada de alocação de memória para o tempo de execução especificado.
title: Função JsSetRuntimeMemoryAllocationCallback | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsSetRuntimeMemoryAllocationCallback
helpviewer_keywords:
- JsSetRuntimeMemoryAllocationCallback function
ms.assetid: 6aa7d58d-6456-4df1-815f-1ba36fb4ae14
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 5c648761473023f00e894fbf75c794cfcc9422c5
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10562007"
---
# Função JsSetRuntimeMemoryAllocationCallback
Define um retorno de chamada de alocação de memória para o tempo de execução especificado.  
  
## Sintaxe  
  
```cpp  
STDAPI_(JsErrorCode) JsSetRuntimeMemoryAllocationCallback(  
   _In_ JsRuntimeHandle runtime,  
   _In_opt_ void *callbackState,  
   _In_ JsMemoryAllocationCallback allocationCallback  
);  
```  
  
#### Parâmetros  
 `runtime`  
 O tempo de execução para o qual registrar o retorno de chamada de alocação.  
  
 `callbackState`  
 Estado fornecido pelo usuário que será devolvido ao retorno de chamada.  
  
 `allocationCallback`  
 Retorno de chamada de alocação de memória a ser chamado para eventos de alocação de memória.  
  
## Valor de retorno  
 O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.  
  
## Comentários  
 O registro de um retorno de chamada de alocação de memória fará com que o Runtime chame de volta para o host sempre que ele adquirir memória de ou liberar memória para o sistema operacional. A rotina de retorno de chamada é chamada antes do Gerenciador de memória de tempo de execução aloca um bloco de memória. A alocação será rejeitada se o retorno de chamada retornar false. O Gerenciador de memória de tempo de execução também invocará a rotina de retorno de chamada após a liberação de um bloco de memória, bem como após a falha de alocação.  
  
 O retorno de chamada é invocado no thread de execução do tempo de execução atual, portanto a execução é bloqueada até que o retorno de chamada seja concluído.  
  
 O valor de retorno do retorno de chamada não é armazenado; as atribuições rejeitadas anteriormente não impedirão que o tempo de execução chame o retorno de chamada novamente mais tarde para novas atribuições de memória.  
  
## Requisitos  
 **Header:** jsrt. h  
  
## Consulte também  
 [Referência (tempo de execução JavaScript)](../chakra-hosting/reference-javascript-runtime.md)