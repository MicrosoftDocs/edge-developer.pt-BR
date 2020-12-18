---
description: Obtém o valor do `true` contexto do script atual.
title: Função JsGetTrueValue | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsGetTrueValue
helpviewer_keywords:
- JsGetTrueValue function
ms.assetid: c2a56d48-344b-492b-90b8-f570710f8310
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 58798e1e8aab57d626be0c8c878f9be39d0af942
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231987"
---
# Função JsGetTrueValue

Obtém o valor do `true` contexto do script atual.  
  
## Sintaxe  
  
```cpp  
STDAPI_(JsErrorCode) JsGetTrueValue(  
   _Out_ JsValueRef *trueValue  
);  
```  
  
#### Parâmetros  
 `trueValue`  
 O `true` valor.  
  
## Valor de retorno  
 O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.  
  
## Comentários  
 Requer um contexto de script ativo.  
  
## Requisitos  
 **Header:** jsrt. h  
  
## Consulte também  
 [Referência (Runtime do JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
