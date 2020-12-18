---
description: Cria um valor de cadeia de caracteres de um ponteiro de cadeia de caracteres.
title: Função JsPointerToString | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsPointerToString
helpviewer_keywords:
- JsPointerToString function
ms.assetid: c71ce07e-4359-450c-afbf-a6ab7d48dddf
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: c00a060098f0b021afca27b300f3e0578e992cb9
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231754"
---
# Função JsPointerToString

Cria um valor de cadeia de caracteres de um ponteiro de cadeia de caracteres.  
  
## Sintaxe  
  
```cpp  
STDAPI_(JsErrorCode) JsPointerToString(  
   _In_reads_(stringLength) const wchar_t *stringValue,  
   _In_ size_t stringLength,  
   _Out_ JsValueRef *value  
);  
```  
  
#### Parâmetros  
 `stringValue`  
 O ponteiro da cadeia de caracteres a ser convertido em um valor de cadeia de caracteres.  
  
 `stringLength`  
 O comprimento da cadeia de caracteres a ser convertida.  
  
 `value`  
 O novo valor de cadeia de caracteres.  
  
## Valor de retorno  
 O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.  
  
## Comentários  
 Requer um contexto de script ativo.  
  
## Requisitos  
 **Header:** jsrt. h  
  
## Consulte também  
 [Referência (Runtime do JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
