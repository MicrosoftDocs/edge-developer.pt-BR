---
description: O contexto passado para o retorno de chamada do aplicativo, JsProjectionEnqueueCallback, de JsRT e, em seguida, passado de volta para JsRT no retorno de chamada fornecido, `JsProjectionCallback` pelo aplicativo na thread correta.
title: Typedef JsProjectionCallbackContext | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 50c705c5-664f-4a1a-92f6-4882fc718ab1
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 58d4c74da13ae0dd269f3c101bbf3d2b95e77732
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561011"
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
 [Referência (tempo de execução JavaScript)](../chakra-hosting/reference-javascript-runtime.md)