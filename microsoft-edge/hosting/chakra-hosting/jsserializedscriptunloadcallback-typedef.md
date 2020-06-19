---
description: Chamado pelo tempo de execução quando ele é concluído com todos os recursos relacionados à execução do script. O chamador deve liberar a origem, se carregada, o código de byte e o contexto no momento.
title: Typedef JsSerializedScriptUnloadCallback | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 8d18c392-cca0-411e-9f2b-0d788b16161a
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: c3da27af18ebc7a1913980a865d926bac6a29d11
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/18/2020
ms.locfileid: "10751937"
---
# Typedef JsSerializedScriptUnloadCallback
Chamado pelo tempo de execução quando ele é concluído com todos os recursos relacionados à execução do script. O chamador deve liberar a origem, se carregada, o código de byte e o contexto no momento.  
  
## Sintaxe  
  
```cpp  
 typedef void (CALLBACK * JsSerializedScriptUnloadCallback)(  
  _In_ JsSourceContext sourceContext  
);  
```  
  
#### Parâmetros  
 `sourceContext`  
 O contexto passado para `JsParseSerializedScriptWithCallback` ou `JsRunSerializedScriptWithCallback` .  
  
## Comentários  
  
> [!WARNING]
## Requisitos  
 **Header:** jsrt. h  
  
## Consulte também  
 [Referência (Runtime do JavaScript)](../chakra-hosting/reference-javascript-runtime.md)