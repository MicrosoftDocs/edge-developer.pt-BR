---
description: O contexto passado para o retorno de chamada do aplicativo, JsProjectionEnqueueCallback, de JsRT e, em seguida, passado de volta para JsRT no retorno de chamada fornecido, `JsProjectionCallback` pelo aplicativo na thread correta.
title: Typedef JsProjectionCallbackContext | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 50c705c5-664f-4a1a-92f6-4882fc718ab1
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 7742b0186a49e99f2738b81357b9e55cfe00042b
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231747"
---
# Typedef JsProjectionCallbackContext

O contexto passado para o retorno de chamada do aplicativo, JsProjectionEnqueueCallback, de JsRT e, em seguida, passado de volta para JsRT no retorno de chamada fornecido, `JsProjectionCallback` pelo aplicativo na thread correta.  
  
## Sintaxe  
  
```cpp  
typedef void *JsProjectionCallbackContext;  
```  
  
## Comentários  
 Requer chamadas `JsSetProjectionEnqueueCallback` para receber chamadas de retorno.  
  
 Essa API só tem suporte no modo EdgeHTML.  
  
## Requisitos  
 jsrt. h  
  
## Consulte também  
 [Referência (Runtime do JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
