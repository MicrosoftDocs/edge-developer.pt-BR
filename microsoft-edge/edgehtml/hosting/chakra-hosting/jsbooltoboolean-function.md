---
description: Cria um valor booliano a partir de um `bool` valor.
title: Função JsBoolToBoolean | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsBoolToBoolean
helpviewer_keywords:
- JsBoolToBoolean function
ms.assetid: 24322ea3-0638-40a3-9b4c-fc912ebed3ff
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 3d6ec9f85d53e0d78c6bbe1c7d3282971831717b
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231442"
---
# Função JsBoolToBoolean

Cria um valor booliano a partir de um `bool` valor.  
  
## Sintaxe  
  
```cpp  
STDAPI_(JsErrorCode JsBoolToBoolean(  
   _In_ bool value,  
   _Out_ JsValueRef *booleanValue  
);  
```  
  
#### Parâmetros  
 `value`  
 O valor a ser convertido.  
  
 `booleanValue`  
 O valor convertido.  
  
## Valor de retorno  
 O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.  
  
## Comentários  
 Requer um contexto de script ativo.  
  
## Requisitos  
 **Header:** jsrt. h  
  
## Consulte também  
 [Referência (Runtime do JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
