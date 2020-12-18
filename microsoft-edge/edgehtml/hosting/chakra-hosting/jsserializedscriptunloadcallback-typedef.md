---
description: Chamado pelo tempo de execução quando ele é concluído com todos os recursos relacionados à execução do script. O chamador deve liberar a origem, se carregada, o código de byte e o contexto no momento.
title: Typedef JsSerializedScriptUnloadCallback | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 8d18c392-cca0-411e-9f2b-0d788b16161a
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 5c63f2ff3faf21a19e31f2f6fd1692e21d59fc0b
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231933"
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
