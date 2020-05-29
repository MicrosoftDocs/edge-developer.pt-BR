---
description: Uma referência a um contexto de script.
title: Typedef JsContextRef | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 8586bfcc-bb24-430d-a6f2-1a3b3e34ec2e
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 80e4b5034079f4f0d26da070bd209aa41bf3475f
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561122"
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
 [Referência (tempo de execução JavaScript)](../chakra-hosting/reference-javascript-runtime.md)