---
description: Adiciona uma referência a um objeto de lixo coletado.
title: Função JsAddRef | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsAddRef
helpviewer_keywords:
- JsAddRef function
ms.assetid: a7f3ed49-6a86-489a-abdf-c99428e79cae
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: fd397dbfeacafdf12728ef0ca2a98d97405f6592
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231456"
---
# Função JsAddRef

Adiciona uma referência a um objeto de lixo coletado.  
  
## Sintaxe  
  
```cpp  
STDAPI_(JsErrorCode) JsAddRef(  
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
 Isso só precisa ser chamado nas `JsRef` alças que não serão armazenadas em algum lugar na pilha. A chamada `JsAddRef` assegura que o objeto ao qual a `JsRef` referência não será liberado até `JsRelease` ser chamado.  
  
## Requisitos  
 **Header:** jsrt. h  
  
## Consulte também  
 [Referência (Runtime do JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
