---
description: Serializa um script analisado para um buffer do que pode ser reutilizado.
title: Função JsSerializeScript | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsSerializeScript
helpviewer_keywords:
- JsSerializeScript function
ms.assetid: ca42c194-e1c1-407d-b542-b9d494e3ac4e
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 236cf40c91256e999d5390acd395b1e97fe538ad
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231932"
---
# Função JsSerializeScript

Serializa um script analisado para um buffer do que pode ser reutilizado.  
  
## Sintaxe  
  
```cpp  
STDAPI_(JsErrorCode) JsSerializeScript(  
   _In_z_ const wchar_t *script,  
   _Out_writes_to_opt_(*bufferSize,  
   *bufferSize) BYTE *buffer,  
   _Inout_ unsigned long *bufferSize  
);  
```  
  
#### Parâmetros  
 `script`  
 O script a ser serializado.  
  
 `buffer`  
 O buffer no qual colocar o script serializado. Pode ser nulo.  
  
 `bufferSize`  
 Na entrada, o tamanho do buffer, em bytes; em Exit, o tamanho do buffer, em bytes, é necessário para armazenar o script serializado.  
  
## Valor de retorno  
 O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.  
  
## Comentários  
 `JsSerializeScript` analisa um script e armazena a forma analisada do script em um formato independente do tempo de execução. O script serializado pode ser desserializado em qualquer tempo de execução sem exigir que o script seja reanalisado.  
  
 Requer um contexto de script ativo.  
  
## Requisitos  
 **Header:** jsrt. h  
  
## Consulte também  
 [Referência (Runtime do JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
