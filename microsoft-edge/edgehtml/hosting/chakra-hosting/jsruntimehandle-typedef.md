---
description: Um identificador para um tempo de execução do Chakra.
title: Typedef JsRuntimeHandle | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 69e59bfd-9b0e-4710-9aa8-fbd6844171bc
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: ab08243505b9699fe07ca2e80f7294adf9eb78ad
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231407"
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
 [Referência (Runtime do JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
