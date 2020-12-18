---
description: O retorno de chamada do aplicativo que é chamado por JsRT quando uma API de projeção é concluída em um thread diferente do original.
title: Typedef JsProjectionEnqueueCallback | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 19c1cefb-a7be-4196-b780-9fe6adf35ba5
caps.latest.revision: 4
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 47527d5e32076e40a82ab5452c2e0f624e8a2818
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231986"
---
# Typedef JsProjectionEnqueueCallback

O retorno de chamada do aplicativo que é chamado por JsRT quando uma API de projeção é concluída em um thread diferente do original.  
  
## Sintaxe  
  
```cpp  
typedef void (CALLBACK *JsProjectionEnqueueCallback)(  
  _In_ JsProjectionCallback jsCallback,  
  _In_ JsProjectionCallbackContext jsContext,  
  _In_opt_ void *callbackState  
);  
```  
  
#### Parâmetros  
 `jsCallback`  
 O retorno de chamada a ser invocado no thread original.  
  
 `jsContext`  
 O contexto do aplicativo.  
  
 `callbackState`  
 O contexto JsRT que deve ser passado `jsCallback` .  
  
## Comentários  
 Requer chamadas JsSetProjectionEnqueueCallback para receber retornos de chamada.  
  
 Essa API só tem suporte no modo EdgeHTML.  
  
## Requisitos  
 jsrt. h  
  
## Consulte também  
 [Referência (Runtime do JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
