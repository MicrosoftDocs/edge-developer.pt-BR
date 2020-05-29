---
description: Inicializa o passado `VARIANT` como uma projeção de um valor JavaScript.
title: Função JsValueToVariant | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsValueToVariant
helpviewer_keywords:
- JsValueToVariant function
ms.assetid: 070244be-a69d-4b78-971b-69c0579c03cf
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: d8748fddcc149cf09fbd46ad3ad489cd66200b71
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10560994"
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
 [Referência (tempo de execução JavaScript)](../chakra-hosting/reference-javascript-runtime.md)