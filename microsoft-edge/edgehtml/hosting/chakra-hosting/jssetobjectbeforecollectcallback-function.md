---
description: Define uma função de retorno de chamada que é chamada pelo tempo de execução antes da coleta de lixo de um objeto.
title: Função JsSetObjectBeforeCollectCallback | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: ea2cbd94-d8b0-4fa9-a4a1-c75a4e338eaf
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 4689184dccaf6bc9f98eeacda5f5a4b91a927d40
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231409"
---
# Função JsSetObjectBeforeCollectCallback

Define uma função de retorno de chamada que é chamada pelo tempo de execução antes da coleta de lixo de um objeto.  
  
## Sintaxe  
  
```cpp  
STDAPI_(JsErrorCode) JsSetObjectBeforeCollectCallback(  
   _In_ JsRef ref,  
   _In_opt_ void *callbackState,  
   _In_ JsObjectBeforeCollectCallback objectBeforeCollectCallback  
);  
```  
  
#### Parâmetros  
 `ref`  
 O objeto para o qual registrar o retorno de chamada.  
  
 `callbackState`  
 Estado fornecido pelo usuário que será devolvido ao retorno de chamada.  
  
 `objectBeforeCollectCallback`  
 A função de retorno de chamada sendo definida. Use NULL para limpar o retorno de chamada registrado anteriormente.  
  
## Valor de retorno  
 O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.  
  
## Comentários  
 O retorno de chamada é invocado no thread de execução do tempo de execução atual, portanto a execução é bloqueada até que o retorno de chamada seja concluído.  
  
 Essa API só tem suporte no modo EdgeHTML.  
  
## Requisitos  
 **Header:** jsrt. h  
  
## Consulte também  
 [Referência (Runtime do JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
