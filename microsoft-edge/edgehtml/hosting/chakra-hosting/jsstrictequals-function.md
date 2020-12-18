---
description: Comparar dois valores JavaScript para igualdade estrita.
title: Função JsStrictEquals | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsStrictEquals
helpviewer_keywords:
- JsStrictEquals function
ms.assetid: b35bc655-7ff8-496a-b678-8950bb976047
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 98af1629129986cc21cafe5660d3155e031919dc
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231581"
---
# Função JsStrictEquals

Comparar dois valores JavaScript para igualdade estrita.  
  
## Sintaxe  
  
```cpp  
STDAPI_(JsErrorCode) JsStrictEquals(  
   _In_ JsValueRef object1,  
   _In_ JsValueRef object2,  
   _Out_ bool *result  
);  
```  
  
#### Parâmetros  
 `object1`  
 O primeiro objeto a ser comparado.  
  
 `object2`  
 O segundo objeto a ser comparado.  
  
 `result`  
 Se os valores são estritamente iguais.  
  
## Valor de retorno  
 O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.  
  
## Comentários  
 Esta função é equivalente à `===` operadora em JavaScript.  
  
 Requer um contexto de script ativo.  
  
## Requisitos  
 **Header:** jsrt. h  
  
## Consulte também  
 [Referência (Runtime do JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
