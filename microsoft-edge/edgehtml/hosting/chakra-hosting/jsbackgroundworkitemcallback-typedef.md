---
description: Um retorno de chamada de item de trabalho em segundo plano.
title: Typedef JsBackgroundWorkItemCallback | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: e6db52e1-830c-46a2-b9f9-cc2d450a1da8
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d69306b334c2e0c9b27b96a5a417739ffdcd7dd7
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231454"
---
# Typedef JsBackgroundWorkItemCallback 

Um retorno de chamada de item de trabalho em segundo plano.  
  
## Sintaxe  
  
```cpp  
typedef void (CALLBACK *JsBackgroundWorkItemCallback)(  
   _In_opt_ void *callbackData  
);  
```  
  
#### Parâmetros  
 callbackData  
 Argumento de dados passado para o serviço de thread.  
  
## Comentários  
 Isso é passado para o serviço de thread do host (se for fornecido) para permitir que o host invoque o retorno de chamada de item de trabalho no thread de segundo plano de sua escolha.  
  
## Requisitos  
 **Header:** jsrt. h  
  
## Consulte também  
 [Referência (Runtime do JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
