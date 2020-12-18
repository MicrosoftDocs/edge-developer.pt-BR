---
description: Uma referência a um contexto de script.
title: Typedef JsContextRef | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 8586bfcc-bb24-430d-a6f2-1a3b3e34ec2e
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: c8a8fcbd67afb150d682cfc19321f0f13acfe3a6
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231443"
---
# Typedef JsContextRef

Uma referência a um contexto de script.  
  
## Sintaxe  
  
```cpp  
typedef JsRef JsContextRef;  
```  
  
## Comentários  
 Cada contexto de script contém seu próprio objeto global, distinto do objeto global em outros contextos de script.  
  
 Muitas APIs de hospedagem Chakra exigem um contexto de script "ativo", que pode ser definido usando `JsSetCurrentContext` . Chakra Hospedagem de APIs que exijam que um contexto atual seja definido notará que, explicitamente, em sua documentação.  
  
## Requisitos  
 **Header:** jsrt. h  
  
## Consulte também  
 [Referência (Runtime do JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
