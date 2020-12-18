---
description: Cria um valor de número de um valor duplo.
title: Função JsDoubleToNumber | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsDoubleToNumber
helpviewer_keywords:
- JsDoubleToNumber function
ms.assetid: 43eb2ee1-2789-4302-954e-c4087e1ee786
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d3385633f41c2e20c43ca865eaeec763b6ff7f43
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231624"
---
# Função JsDoubleToNumber

Cria um valor numérico a partir de um `double` valor.  
  
## Sintaxe  
  
```cpp  
STDAPI_(JsErrorCode) JsDoubleToNumber(  
   _In_ double doubleValue,  
   _Out_ JsValueRef *value  
);  
```  
  
#### Parâmetros  
 `doubleValue`  
 A `double` para converter para um valor numérico.  
  
 `value`  
 O novo valor numérico.  
  
## Valor de retorno  
 O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.  
  
## Comentários  
 Requer um contexto de script ativo.  
  
## Requisitos  
 **Header:** jsrt. h  
  
## Consulte também  
 [Referência (Runtime do JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
