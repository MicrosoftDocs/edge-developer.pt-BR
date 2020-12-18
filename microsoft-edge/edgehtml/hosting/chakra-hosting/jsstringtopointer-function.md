---
description: Recupera o ponteiro da cadeia de caracteres de um valor de cadeia de caracteres.
title: Função JsStringToPointer | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsStringToPointer
helpviewer_keywords:
- JsStringToPointer function
ms.assetid: c7aa7a09-489d-4435-8f8a-aeb62f8875ae
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 77b8e16be41d8b5541129b50fa200b947f566342
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231578"
---
# Função JsStringToPointer

Recupera o ponteiro da cadeia de caracteres de um valor de cadeia de caracteres.  
  
## Sintaxe  
  
```cpp  
STDAPI_(JsErrorCode) JsStringToPointer(  
   _In_ JsValueRef value,  
   _Outptr_result_buffer_(*stringLength) const wchar_t **stringValue,  
   _Out_ size_t *stringLength  
);  
```  
  
#### Parâmetros  
 `value`  
 O valor da cadeia de caracteres a ser convertido em um ponteiro de cadeia de caracteres.  
  
 `stringValue`  
 O ponteiro da cadeia de caracteres.  
  
 `stringLength`  
 O comprimento da cadeia de caracteres.  
  
## Valor de retorno  
 O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.  
  
## Comentários  
 Esta função recupera o ponteiro da cadeia de caracteres de um valor de cadeia de caracteres. Ele falhará `JsErrorInvalidArgument` se o tipo do valor não for cadeia de caracteres. O tempo de vida da cadeia de caracteres retornado será o mesmo do tempo de vida do valor que veio, mas o ponteiro da cadeia de caracteres não será considerado uma referência para o valor (e, portanto, não o deixará de ser coletado).  
  
 Requer um contexto de script ativo.  
  
## Requisitos  
 **Header:** jsrt. h  
  
## Consulte também  
 [Referência (Runtime do JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
