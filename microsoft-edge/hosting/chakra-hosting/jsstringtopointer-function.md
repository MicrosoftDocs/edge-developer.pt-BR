---
description: Recupera o ponteiro da cadeia de caracteres de um valor de cadeia de caracteres.
title: Função JsStringToPointer | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsStringToPointer
helpviewer_keywords:
- JsStringToPointer function
ms.assetid: c7aa7a09-489d-4435-8f8a-aeb62f8875ae
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 1f5997894c4ea479378a323b230492dde28ab177
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10562003"
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
 [Referência (tempo de execução JavaScript)](../chakra-hosting/reference-javascript-runtime.md)