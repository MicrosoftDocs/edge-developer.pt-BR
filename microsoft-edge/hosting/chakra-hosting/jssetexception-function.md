---
description: Define o tempo de execução do contexto atual como um estado de exceção.
title: Função JsSetException | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsSetException
helpviewer_keywords:
- JsSetException function
ms.assetid: c528793a-2e1b-4ee1-bd2e-e63fd547dc40
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 75d2895a725c622a0b46887d10154c3a0c56c7e9
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10562114"
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
 [Referência (tempo de execução JavaScript)](../chakra-hosting/reference-javascript-runtime.md)