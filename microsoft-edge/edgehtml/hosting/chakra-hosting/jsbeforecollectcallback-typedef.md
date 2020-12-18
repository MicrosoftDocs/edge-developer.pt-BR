---
description: Um retorno de chamada chamado antes da coleta.
title: Typedef JsBeforeCollectCallback | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 58bece47-4e6d-49e7-a93d-b6a8f9928b41
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 23ed386a6a28d356aa80cf85650a981d4836a6b6
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231445"
---
# Typedef JsBeforeCollectCallback

Um retorno de chamada chamado antes da coleta.  
  
## Sintaxe  
  
```cpp  
typedef void (CALLBACK *JsBeforeCollectCallback)(  
_In_opt_ void *callbackState  
);  
```  
  
#### Parâmetros  
 callbackstate  
 O estado passado para JsSetBeforeCollectCallback.  
  
## Comentários  
 Use JsSetBeforeCollectCallback para registrar esse retorno de chamada.  
  
## Requisitos  
 **Header:** jsrt. h  
  
## Consulte também  
 [Referência (Runtime do JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
