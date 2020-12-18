---
description: Descarta um tempo de execução.
title: Função JsDisposeRuntime | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsDisposeRuntime
helpviewer_keywords:
- JsDisposeRuntime function
ms.assetid: 0aefde3f-7250-48be-afc5-53ea85c12f30
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 8cff4578415cdf1aaa01b7203ce734cef9115301
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231626"
---
# Função JsDisposeRuntime

Descarta um tempo de execução.  
  
## Sintaxe  
  
```cpp  
STDAPI_(JsErrorCode) JsDisposeRuntime(  
   _In_ JsRuntimeHandle runtime  
);  
```  
  
#### Parâmetros  
 `runtime`  
 O tempo de execução a ser Descartado.  
  
## Valor de retorno  
 O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.  
  
## Comentários  
 Depois que um tempo de execução é Descartado, todos os recursos pertencentes a ele são inválidos e não podem ser usados. Se o tempo de execução estiver ativo (ou seja, estiver definido como atual em um determinado thread), ele não poderá ser Descartado.  
  
## Requisitos  
 **Header:** jsrt. h  
  
## Consulte também  
 [Referência (Runtime do JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
