---
description: Um identificador para um tempo de execução do Chakra.
title: Typedef JsRuntimeHandle | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 69e59bfd-9b0e-4710-9aa8-fbd6844171bc
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 4ccdcf39ec6062db47e1b9de249d75c8804de405
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10562122"
---
# Typedef JsRuntimeHandle
Um identificador para um tempo de execução do Chakra.  
  
## Sintaxe  
  
```cpp  
typedef void *JsRuntimeHandle;  
```  
  
## Comentários  
 Cada tempo de execução do Chakra tem seu próprio mecanismo de execução independente, compilador JIT e heap de lixo coletado. Dessa forma, cada tempo de execução é completamente isolado de outros tempos de execução.  
  
 Os tempos de execução podem ser usados em qualquer thread, mas somente um thread pode chamar em um tempo de execução a qualquer momento.  
  
> [!WARNING]
>  Um JsRuntimeHandle, diferentemente de outras referências a objetos na API de hospedagem do Chakra, não é coletado como lixo, já que contém o próprio heap coletado pelo Garbage Collector. Um tempo de execução continuará a existir até que o JsDisposeRuntime seja chamado.  
  
## Requisitos  
 **Header:** jsrt. h  
  
## Consulte também  
 [Referência (tempo de execução JavaScript)](../chakra-hosting/reference-javascript-runtime.md)