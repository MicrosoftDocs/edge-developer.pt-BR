---
description: O retorno de chamada JsRT que deve ser chamado com o contexto passado para `JsProjectionEnqueueCallback` o thread correto.
title: Typedef JsProjectionCallback | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 32f22d37-e57e-4196-b6cd-a3fc75bd0632
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: b30f9a7dc4671896eeacecbf58ef88f0383e9e7e
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561010"
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
 [Referência (tempo de execução JavaScript)](../chakra-hosting/reference-javascript-runtime.md)