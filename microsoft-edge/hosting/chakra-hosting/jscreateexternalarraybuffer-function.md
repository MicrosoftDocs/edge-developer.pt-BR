---
description: Cria um `ArrayBuffer` objeto JavaScript para acessar a memória externa.
title: Função JsCreateExternalArrayBuffer | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 4a02aaec-0f67-4bf9-b37c-71cdb1410ca4
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 376eedda18393436d9dce340753586bf32599b21
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561099"
---
# Função JsCreateExternalArrayBuffer
Cria um `ArrayBuffer` objeto JavaScript para acessar a memória externa.
  
## Sintaxe  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateExternalArrayBuffer(  
  _Pre_maybenull_ _Pre_writable_byte_size_(byteLength) void *data,  
  _In_ unsigned int byteLength,  
  _In_opt_ JsFinalizeCallback finalizeCallback,  
  _In_opt_ void *callbackState,  
  _Out_ JsValueRef *result  
);  
  
```  
  
#### Parâmetros  
 `data`  
 Um ponteiro para a memória externa.  
  
 `byteLength`  
 O número de bytes na memória externa.  
  
 `finalizeCallback`  
 Um retorno de chamada para quando o objeto for finalizado. Pode ser nulo.  
  
 `callbackState`  
 Estado fornecido pelo usuário que será devolvido para finalizeCallback.  
  
 `result`  
 O novo `ArrayBuffer` objeto.  
  
## Valor de retorno  
 O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.  
  
## Comentários  
 Requer um contexto de script ativo.  
  
## Requisitos  
 **Header:** jsrt. h  
  
## Consulte também  
 [Referência (tempo de execução JavaScript)](../chakra-hosting/reference-javascript-runtime.md)