---
description: Um retorno de chamada de serviço de thread.
title: Typedef JsThreadServiceCallback | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: dbe67be5-418a-4f66-8b68-b38078a6d140
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: a5f1fe416e158e9524bdd1caab847977a5dd21b8
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231576"
---
# Typedef JsThreadServiceCallback

Um retorno de chamada de serviço de thread.  
  
## Sintaxe  
  
```cpp  
typedef bool (CALLBACK *JsThreadServiceCallback)(  
   _In_ JsBackgroundWorkItemCallback callback,  
   _In_opt_ void *callbackData  
);  
```  
  
#### Parâmetros  
 retorno  
 O retorno de chamada do item de trabalho em segundo plano.  
  
 callbackData  
 O argumento de dados a ser passado para o retorno de chamada.  
  
## Comentários  
 O host pode especificar um serviço de thread de segundo plano ao chamar JsCreateRuntime. Se especificado, os itens de trabalho em segundo plano serão passados para o host usando esse retorno de chamada. O host é esperado para começar a executar o item de trabalho em segundo plano imediatamente e retornar true ou retornar false e o tempo de execução manipulará o item de trabalho no-thread.  
  
## Requisitos  
 **Header:** jsrt. h  
  
## Consulte também  
 [Referência (Runtime do JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
