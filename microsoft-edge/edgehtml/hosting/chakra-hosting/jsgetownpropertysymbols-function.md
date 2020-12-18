---
description: Obtém a lista de todas as propriedades de símbolo no objeto.
title: Função JsGetOwnPropertySymbols | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 57c431e3-de0b-4ed0-b750-87a86448daff
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d44da140f61a17d4cdc3a959c8fa7d017cbab1cc
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231790"
---
# Função JsGetOwnPropertySymbols

Obtém a lista de todas as propriedades de símbolo no objeto.  
  
## Sintaxe  
  
```cpp  
STDAPI_(JsErrorCode) JsGetOwnPropertySymbols(  
   _In_ JsValueRef object,  
   _Out_ JsValueRef *propertySymbols  
);  
```  
  
#### Parâmetros  
 `object`  
 O objeto do qual obter os símbolos de propriedade.  
  
 `propertySymbols`  
 Uma matriz de símbolos de propriedade.  
  
## Valor de retorno  
 O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.  
  
## Comentários  
 Requer um contexto de script ativo.  
  
 Essa API só tem suporte no modo Microsoft Edge.  
  
## Requisitos  
 **Header:** jsrt. h  
  
## Consulte também  
 [Referência (Runtime do JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
