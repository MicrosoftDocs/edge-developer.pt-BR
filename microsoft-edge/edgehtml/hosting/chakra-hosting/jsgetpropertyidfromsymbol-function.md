---
description: Obtém a ID da propriedade associada ao símbolo.
title: Função JsGetPropertyIdFromSymbol | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 190fe4b9-352e-4b10-9d0e-6c6bbd6363e8
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d97f1fb517164d692cdd010f899dc40d2e3596ed
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231808"
---
# Função JsGetPropertyIdFromSymbol

Obtém a ID da propriedade associada ao símbolo.  
  
## Sintaxe  
  
```cpp  
STDAPI_(JsErrorCode) JsGetPropertyIdFromSymbol(  
   _In_ JsValueRef symbol,  
   _Out_ JsPropertyIdRef *propertyId  
);  
```  
  
#### Parâmetros  
 `symbol`  
 O símbolo cuja ID de propriedade está sendo recuperada.  
  
 `propertyId`  
 A ID da propriedade para o símbolo fornecido.  
  
## Valor de retorno  
 O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.  
  
## Comentários  
 As IDs de propriedade são específicas de um contexto e não podem ser usadas em contextos.  
  
 Requer um contexto de script ativo.  
  
 Essa API só tem suporte no modo Microsoft Edge.  
  
## Requisitos  
 **Header:** jsrt. h  
  
## Consulte também  
 [Referência (Runtime do JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
