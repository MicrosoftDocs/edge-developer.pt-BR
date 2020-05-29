---
description: Tipo de evento de retorno de chamada de atribuição.
title: Enumeração JsMemoryEventType | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsMemoryEventType
helpviewer_keywords:
- JsMemoryEventType enumeration
ms.assetid: b4b176b6-b536-472e-8999-95b681a1df55
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 1e9833777ed8fe5a19fd2a1487715296279f7351
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561018"
---
# Enumeração JsMemoryEventType
Tipo de evento de retorno de chamada de atribuição.  
  
## Sintaxe  
  
```cpp  
enum JsMemoryEventType;  
```  
  
## Parte  
  
### Valores  
  
|Nome|Descrição|  
|----------|-----------------|  
|`JsMemoryAllocate`|Indica uma solicitação de alocação de memória.|  
|`JsMemoryFailure`|Indica um evento de alocação com falha.|  
|`JsMemoryFree`|Indica um evento de liberação de memória.|  
  
## Requisitos  
 **Header:** jsrt. h  
  
## Consulte também  
 [Referência (tempo de execução JavaScript)](../chakra-hosting/reference-javascript-runtime.md)