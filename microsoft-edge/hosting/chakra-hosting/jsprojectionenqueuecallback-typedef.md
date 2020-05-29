---
description: O retorno de chamada do aplicativo que é chamado por JsRT quando uma API de projeção é concluída em um thread diferente do original.
title: Typedef JsProjectionEnqueueCallback | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 19c1cefb-a7be-4196-b780-9fe6adf35ba5
caps.latest.revision: 4
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 064a7d1077ae5222e44ab08ebe0592bb97b1f2af
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561009"
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
 [Referência (tempo de execução JavaScript)](../chakra-hosting/reference-javascript-runtime.md)