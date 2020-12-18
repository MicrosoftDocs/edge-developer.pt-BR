---
description: Chamado pelo tempo de execução para carregar o código-fonte do script serializado. O chamador deve manter o buffer do script válido até que o `JsSerializedScriptUnloadCallback` .
title: Typedef JsSerializedScriptLoadSourceCallback | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 9406c488-76ac-49e5-b305-39751f3412ea
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 2bb30befc61003d20cdeaa293fd1fdfdc95b36f7
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231983"
---
# Typedef JsSerializedScriptLoadSourceCallback

Chamado pelo tempo de execução para carregar o código-fonte do script serializado. O chamador deve manter o buffer do script válido até que o `JsSerializedScriptUnloadCallback` .  
  
## Sintaxe  
  
```cpp  
typedef bool (CALLBACK * JsSerializedScriptLoadSourceCallback)(  
  _In_ JsSourceContextsourceContext,  
  _Outptr_result_z_ const wchar_t** scriptBuffer  
);  
```  
  
#### Parâmetros  
 `sourceContext`  
 O contexto passado para `JsParseSerializedScriptWithCallback` ou `JsRunSerializedScriptWithCallback` .  
  
 `scriptBuffer`  
 O script retornou.  
  
## Comentários  
  
> [!WARNING]
## Requisitos  
 **Header:** jsrt. h  
  
## Consulte também  
 [Referência (Runtime do JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
