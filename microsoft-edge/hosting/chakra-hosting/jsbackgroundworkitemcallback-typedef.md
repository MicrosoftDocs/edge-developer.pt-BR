---
description: Um retorno de chamada de item de trabalho em segundo plano.
title: Typedef JsBackgroundWorkItemCallback | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: e6db52e1-830c-46a2-b9f9-cc2d450a1da8
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 9bc1e5687d92d7286e1e6d4387bd6b69d95ceb68
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561135"
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
 [Referência (tempo de execução JavaScript)](../chakra-hosting/reference-javascript-runtime.md)