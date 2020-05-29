---
description: Cria um `DataView` objeto JavaScript.
title: Função JsCreateDataView | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 161e59eb-d429-46f7-9a38-bbf2149ccf44
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 1bf237458e8561b7070e4f3f0d4a14050f028375
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561105"
---
# Função JsCreateDataView
Cria um `DataView` objeto JavaScript.  
  
## Sintaxe  
  
```cpp  
JsErrorCode  JsCreateDataView(  
   _In_ JsValueRef arrayBuffer,  
   _In_ unsigned int byteOffset,  
   _In_ unsigned int byteLength,  
   _Out_ JsValueRef *result  
);  
```  
  
#### Parâmetros  
 `arrayBuffer`  
 Um `ArrayBuffer` objeto existente a ser usado como armazenamento para o objeto de resultado `DataView` .  
  
 `byteOffset`  
 O offset em bytes do início do `arrayBuffer` para o resultado `DataView` para referência.  
  
 `byteLength`  
 O número de bytes em ArrayBuffer para o DataView do resultado fazer referência.  
  
 `result`  
 O novo objeto DataView.  
  
## Valor de retorno  
 O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.  
  
## Comentários  
 Requer um contexto de script ativo.  
  
 Essa API só tem suporte no modo Microsoft Edge.  
  
## Requisitos  
 **Header:** jsrt. h  
  
## Consulte também  
 [Referência (tempo de execução JavaScript)](../chakra-hosting/reference-javascript-runtime.md)