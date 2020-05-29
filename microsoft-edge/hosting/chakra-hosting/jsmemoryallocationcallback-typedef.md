---
description: Rotina de retorno de chamada implementada pelo usuário para eventos de alocação de memória.
title: Typedef JsMemoryAllocationCallback | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 511babc7-3caa-4ee5-82a2-943bbd34db8d
caps.latest.revision: 7
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: b11b3d076c01dbfcae190fd665528323d6f8b987
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561021"
---
# Typedef JsMemoryAllocationCallback
Rotina de retorno de chamada implementada pelo usuário para eventos de alocação de memória.  
  
## Sintaxe  
  
```cpp  
typedef bool (CALLBACK * JsMemoryAllocationCallback)(  
   _In_opt_ void *callbackState,  
   _In_ JsMemoryEventType allocationEvent,  
   _In_ size_t allocationSize  
);  
```  
  
#### Parâmetros  
 callbackstate  
 O estado passado para JsSetRuntimeMemoryAllocationCallback.  
  
 allocationEvent  
 O tipo de evento de alocação de tipo.  
  
 inlocatione  
 O tamanho da alocação.  
  
## Valor da propriedade/valor de retorno  
 Para o evento JsMemoryAllocate, retornar true permite que o tempo de execução continue com a alocação. Retornar false indica que a solicitação de alocação foi rejeitada. O valor de retorno é ignorado para outros eventos de alocação.  
  
## Comentários  
 Use JsSetRuntimeMemoryAllocationCallback para registrar esse retorno de chamada.  
  
## Requisitos  
 **Header:** jsrt. h  
  
## Consulte também  
 [Referência (tempo de execução JavaScript)](../chakra-hosting/reference-javascript-runtime.md)