---
description: Define o limite de memória atual para um tempo de execução.
title: Função JsSetRuntimeMemoryLimit | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsSetRuntimeMemoryLimit
helpviewer_keywords:
- JsSetRuntimeMemoryLimit function
ms.assetid: 74feb31f-19f6-43e3-b117-0694c59ac593
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: ec8d098c528ac813926797280541aa2c9c4fee79
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10562006"
---
# Função JsSetRuntimeMemoryLimit
Define o limite de memória atual para um tempo de execução.  
  
## Sintaxe  
  
```cpp  
STDAPI_(JsErrorCode) JsSetRuntimeMemoryLimit(  
   _In_ JsRuntimeHandle runtime,  
   _In_ size_t memoryLimit  
);  
```  
  
#### Parâmetros  
 `runtime`  
 O tempo de execução cujo limite de memória deve ser definido.  
  
 `memoryLimit`  
 O novo limite de memória em tempo de execução, em bytes ou-1 para nenhum limite de memória.  
  
## Valor de retorno  
 O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.  
  
## Comentários  
 Um limite de memória causará qualquer operação que exceda o limite de falha com um erro de "memória insuficiente". Definir o limite de memória do tempo de execução para-1 significa que o tempo de execução não tem limite de memória. Novos tempos de execução padrão para não ter limite de memória. Se o novo limite de memória exceder o uso atual, a chamada será bem-sucedida e todas as atribuições futuras nesse tempo de execução falharão até que o uso da memória do tempo de execução fique abaixo do limite.  
  
 O limite de memória do tempo de execução pode ser sempre definido, independentemente do tempo de execução estar ativo ou não em outro thread.  
  
## Requisitos  
 **Header:** jsrt. h  
  
## Consulte também  
 [Referência (tempo de execução JavaScript)](../chakra-hosting/reference-javascript-runtime.md)