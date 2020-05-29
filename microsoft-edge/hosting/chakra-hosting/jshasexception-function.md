---
description: Determina se o tempo de execução do contexto atual está em um estado de exceção.
title: Função JsHasException | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsHasException
helpviewer_keywords:
- JsHasException function
ms.assetid: ac7da3ce-c746-4154-bbb8-bcb0859a8d5b
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 25ddb8f9cc407dd414a6cd2210c315eb4dd7b141
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10562163"
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
 [Referência (tempo de execução JavaScript)](../chakra-hosting/reference-javascript-runtime.md)