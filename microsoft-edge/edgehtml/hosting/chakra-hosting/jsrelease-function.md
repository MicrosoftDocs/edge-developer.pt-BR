---
description: Libera uma referência a um objeto coletado pelo Garbage Collector.
title: Função JsRelease | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsRelease
helpviewer_keywords:
- JsRelease function
ms.assetid: 8714fd0b-5b66-48e0-927e-7b93af6cde7b
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 46552a03dc56a10b1d258d8c33da1c533f38464a
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231404"
---
# Função JsRelease

Libera uma referência a um objeto coletado pelo Garbage Collector.  
  
## Sintaxe  
  
```cpp  
STDAPI_(JsErrorCode) JsRelease(  
   _In_ JsRef ref,  
   _Out_opt_ unsigned int *count  
);  
```  
  
#### Parâmetros  
 `ref`  
 O objeto ao qual adicionar uma referência.  
  
 `count`  
 A nova contagem de referência do objeto (pode passar nulo).  
  
## Valor de retorno  
 O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.  
  
## Comentários  
 Remove uma referência a um `JsRef` identificador criado por `JsAddRef` .  
  
## Requisitos  
 **Header:** jsrt. h  
  
## Consulte também  
 [Referência (Runtime do JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
