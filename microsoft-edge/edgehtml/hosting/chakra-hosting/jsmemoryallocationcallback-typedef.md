---
description: Rotina de retorno de chamada implementada pelo usuário para eventos de alocação de memória.
title: Typedef JsMemoryAllocationCallback | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 511babc7-3caa-4ee5-82a2-943bbd34db8d
caps.latest.revision: 7
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 22b5cc0fe5a2c8b49f71c91d28f95ba29af37849
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231422"
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
 [Referência (Runtime do JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
