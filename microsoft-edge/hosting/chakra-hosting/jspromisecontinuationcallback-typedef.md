---
description: Um retorno de chamada de continuação da Promise.
title: Typedef JsPromiseContinuationCallback | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 51a3fd02-9668-4cf7-bb0b-e1fd03b2528f
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 023d88af5ff82056d8f57453e0a53b91b34565a6
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561003"
---
# Typedef JsPromiseContinuationCallback
Um retorno de chamada de continuação da Promise.  
  
## Sintaxe  
  
```cpp  
typedef void (CALLBACK *JsPromiseContinuationCallback)(  
  _In_ JsValueRef task,  
  _In_opt_ void *callbackState  
);  
```  
  
#### Parâmetros  
 `task`  
  `callbackState`  
  
## Comentários  
 O host pode especificar um retorno de chamada de continuação Promise em `JsSetPromiseContinuationCallback` . Se um script criar uma tarefa para ser executada mais tarde, o retorno de chamada de continuação Promise será chamado com a tarefa e a tarefa deverá ser inserida em uma fila FIFO para ser executada quando o script atual for executado.  
  
 Essa API só tem suporte no modo EdgeHTML.  
  
## Requisitos  
 jsrt. h  
  
## Consulte também  
 [Referência (tempo de execução JavaScript)](../chakra-hosting/reference-javascript-runtime.md)