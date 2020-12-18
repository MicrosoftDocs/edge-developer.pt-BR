---
description: Retorna um valor que indica se a execução do script está desabilitada no tempo de execução.
title: Função JsIsRuntimeExecutionDisabled | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsIsRuntimeExecutionDisabled
helpviewer_keywords:
- JsIsRuntimeExecutionDisabled function
ms.assetid: 77490280-fb84-4614-a1f0-6ac31e3bd607
caps.latest.revision: 5
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 0ce59c77525abdb2dd6cac71dde1378264395e79
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231246"
---
# Função JsIsRuntimeExecutionDisabled

Retorna um valor que indica se a execução do script está desabilitada no tempo de execução.  
  
## Sintaxe  
  
```cpp  
STDAPI_(JsErrorCode) JsIsRuntimeExecutionDisabled(    _In_ JsRuntimeHandle runtime,    _Out_ bool *isDisabled);  
```  
  
#### Parâmetros  
 `runtime`  
 Especifica o tempo de execução para verificar se a execução está desabilitada.  
  
 `isDisabled`  
 `true` se a execução estiver desabilitada, `false` caso contrário.  
  
## Valor de retorno  
 `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.  
  
## Requisitos  
 **Header:** jsrt. h  
  
## Consulte também  
 [Referência (Runtime do JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
