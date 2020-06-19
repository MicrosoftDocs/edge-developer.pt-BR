---
description: Chamado pelo tempo de execução para carregar o código-fonte do script serializado. O chamador deve manter o buffer do script válido até que o `JsSerializedScriptUnloadCallback` .
title: Typedef JsSerializedScriptLoadSourceCallback | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 9406c488-76ac-49e5-b305-39751f3412ea
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 571314145cc19513f04174a9a1c93822a5795b29
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752196"
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