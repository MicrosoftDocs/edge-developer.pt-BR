---
description: Um retorno de chamada chamado antes de coletar um objeto.
title: Typedef JsObjectBeforeCollectCallback | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: f21a064a-579f-44cb-9d21-76b62e8c18f5
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 4c24385ec5e15919719ffb0ae71c8adf39c1724c
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231761"
---
# Typedef JsObjectBeforeCollectCallback

Um retorno de chamada chamado antes de coletar um objeto.  
  
## Sintaxe  
  
```cpp  
typedef void (CALLBACK *JsObjectBeforeCollectCallback)(  
  _In_ JsRef ref,  
  _In_opt_ void *callbackState  
);  
```  
  
#### Parâmetros  
 `ref`  
 O objeto a ser coletado.  
  
 `callbackState`  
 O estado passado para `JsSetObjectBeforeCollectCallback` .  
  
## Comentários  
 Essa API só tem suporte no modo EdgeHTML.  
  
## Requisitos  
 jsrt. h  
  
## Consulte também  
 [Referência (Runtime do JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
