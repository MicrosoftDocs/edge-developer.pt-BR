---
description: Um retorno de chamada de serviço de thread.
title: Typedef JsThreadServiceCallback | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: dbe67be5-418a-4f66-8b68-b38078a6d140
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 5eb9f2986c79db024f01f4d22050f79c9689400c
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561001"
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
 [Referência (tempo de execução JavaScript)](../chakra-hosting/reference-javascript-runtime.md)