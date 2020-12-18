---
description: Cria uma nova função JavaScript com Name.
title: Função JsCreateNamedFunction | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 72f40d06-ab82-4fed-a632-68af6b4126c2
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: b54add359422a9312a0ded641051fd04585f3d7e
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231562"
---
# Função JsCreateNamedFunction

Cria uma nova função JavaScript com Name.
  
## Sintaxe  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateNamedFunction(  
   _In_ JsValueRef name,  
   _In_ JsNativeFunction nativeFunction,  
   _In_opt_ void *callbackState,  
   _Out_ JsValueRef *function  
);  
```  
  
#### Parâmetros  
 `name`  
 O nome desta função que será usado para diagnóstico e propósitos de cadeia de caracteres.  
  
 `nativeFunction`  
 O método a ser chamado quando a função é invocada.  
  
 `callbackState`  
 Estado fornecido pelo usuário que será devolvido ao retorno de chamada.  
  
 `function`  
 O novo objeto function.  
  
## Valor de retorno  
  
## Comentários  
 Requer um contexto de script ativo.  
  
 Essa API só tem suporte no modo Microsoft Edge.  
  
## Requisitos  
 **Header:** jsrt. h  
  
## Consulte também  
 [Referência (Runtime do JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
