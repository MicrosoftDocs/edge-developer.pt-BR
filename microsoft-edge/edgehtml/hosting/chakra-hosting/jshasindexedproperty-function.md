---
description: Testa se um objeto tem um valor no índice especificado.
title: Função JsHasIndexedProperty | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsHasIndexedProperty
helpviewer_keywords:
- JsHasIndexedProperty function
ms.assetid: 30436a3d-fda0-407e-aba2-142be2310372
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 9eb1794c465b4b116978a2150285e2fed3ae1d9b
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231635"
---
# Função JsHasIndexedProperty

Testa se um objeto tem um valor no índice especificado.  
  
## Sintaxe  
  
```cpp  
STDAPI_(JsErrorCode) JsHasIndexedProperty(  
   _In_ JsValueRef object,  
   _In_ JsValueRef index,  
   _Out_ bool *result  
);  
```  
  
#### Parâmetros  
 `object`  
 O objeto no qual operar.  
  
 `index`  
 O índice a ser testado.  
  
 `result`  
 Se o objeto tem um valor no índice especificado.  
  
## Valor de retorno  
 O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.  
  
## Comentários  
 Requer um contexto de script ativo.  
  
## Requisitos  
 **Header:** jsrt. h  
  
## Consulte também  
 [Referência (Runtime do JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
