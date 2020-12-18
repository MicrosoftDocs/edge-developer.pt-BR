---
description: Cria um `DataView` objeto JavaScript.
title: Função JsCreateDataView | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 161e59eb-d429-46f7-9a38-bbf2149ccf44
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 1d6d170d53f3bfaf885713b6f3abca0b066f8c1d
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231420"
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
 [Referência (Runtime do JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
