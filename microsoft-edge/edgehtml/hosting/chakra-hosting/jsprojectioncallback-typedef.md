---
description: O retorno de chamada JsRT que deve ser chamado com o contexto passado para `JsProjectionEnqueueCallback` o thread correto.
title: Typedef JsProjectionCallback | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 32f22d37-e57e-4196-b6cd-a3fc75bd0632
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 211325b536dc84340974b02973f1de9d5749a60a
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231751"
---
# Typedef JsProjectionCallback

O retorno de chamada JsRT que deve ser chamado com o contexto passado para `JsProjectionEnqueueCallback` o thread correto.  
  
## Sintaxe  
  
```cpp  
typedef void (CALLBACK *JsProjectionCallback)(  
  _In_ JsProjectionCallbackContext jsContext  
);  
```  
  
#### Parâmetros  
 `jsContext`  
 Requer chamadas `JsSetProjectionEnqueueCallback` para receber chamadas de retorno.  
  
## Comentários  
 Essa API só tem suporte no modo EdgeHTML.  
  
## Requisitos  
 jsrt. h  
  
## Consulte também  
 [Referência (Runtime do JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
