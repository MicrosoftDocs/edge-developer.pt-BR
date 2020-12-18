---
description: Inicializa o passado `VARIANT` como uma projeção de um valor JavaScript.
title: Função JsValueToVariant | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsValueToVariant
helpviewer_keywords:
- JsValueToVariant function
ms.assetid: 070244be-a69d-4b78-971b-69c0579c03cf
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: f383f2d8bc3aab70b4a361b370698cd71cb714d3
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231574"
---
# Função JsValueToVariant

Inicializa o passado `VARIANT` como uma projeção de um valor JavaScript.  
  
## Sintaxe  
  
```cpp  
STDAPI_(JsErrorCode) JsValueToVariant(  
   _In_ JsValueRef object,  
   _Out_ VARIANT *variant  
);  
```  
  
#### Parâmetros  
 `object`  
 Um valor JavaScript para projetar como `VARIANT` .  
  
 `variant`  
 Um ponteiro para uma `VARIANT` estrutura que será inicializada como uma projeção.  
  
## Valor de retorno  
  
## Comentários  
 A projeção `VARIANT` pode ser usada por clientes de automação com para chamar o objeto JavaScript projetado.  
  
 Requer um contexto de script ativo.  
  
## Requisitos  
 **Header:** jsrt. h  
  
## Consulte também  
 [Referência (Runtime do JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
