---
description: Um retorno de chamada de continuação da Promise.
title: Typedef JsPromiseContinuationCallback | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 51a3fd02-9668-4cf7-bb0b-e1fd03b2528f
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: da121d186cd9d0ab1a9770be08c9a92b52cf3366
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231984"
---
# Typedef JsPromiseContinuationCallback

Um retorno de chamada de continuação da Promise.  
  
## Sintaxe  
  
```cpp  
typedef void (CALLBACK *JsPromiseContinuationCallback)(  
  _In_ JsValueRef task,  
  _In_opt_ void *callbackState  
);  
```  
  
#### Parâmetros  
 `task`  
  `callbackState`  
  
## Comentários  
 O host pode especificar um retorno de chamada de continuação Promise em `JsSetPromiseContinuationCallback` . Se um script criar uma tarefa para ser executada mais tarde, o retorno de chamada de continuação Promise será chamado com a tarefa e a tarefa deverá ser inserida em uma fila FIFO para ser executada quando o script atual for executado.  
  
 Essa API só tem suporte no modo EdgeHTML.  
  
## Requisitos  
 jsrt. h  
  
## Consulte também  
 [Referência (Runtime do JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
