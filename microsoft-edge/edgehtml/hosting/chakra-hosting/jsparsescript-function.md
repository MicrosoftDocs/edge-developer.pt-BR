---
description: Analisa um script e retorna uma função que representa o script.
title: Função JsParseScript | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsParseScript
helpviewer_keywords:
- JsParseScript function
ms.assetid: e9d0e363-7cbe-43eb-9dc0-1f47e586c9ab
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 656d9a992868a3cb892808775f160092b8eaf069
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231757"
---
# Função JsParseScript

Analisa um script e retorna uma função que representa o script.  
  
## Sintaxe  
  
```cpp  
STDAPI_(JsErrorCode) JsParseScript(  
   _In_z_ const wchar_t *script,  
   _In_ JsSourceContext sourceContext,  
   _In_z_ const wchar_t *sourceUrl,  
   _Out_ JsValueRef *result  
);  
```  
  
#### Parâmetros  
 `script`  
 O script a ser analisado.  
  
 `sourceContext`  
 Um cookie identificando o script que pode ser usado por contextos de script debuggable.  
  
 `sourceUrl`  
 O local de onde o script veio.  
  
 `result`  
 Uma função que representa o código de script.  
  
## Valor de retorno  
 O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.  
  
## Comentários  
 Requer um contexto de script ativo.  
  
## Requisitos  
 **Header:** jsrt. h  
  
## Consulte também  
 [Referência (Runtime do JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
