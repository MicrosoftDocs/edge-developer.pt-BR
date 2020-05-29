---
description: Cria um objeto matriz tipada JavaScript.
title: Função JsCreateTypedArray | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 937a2a91-6f5f-4aaa-a018-d3089702bf36
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 57c5d15d76bf8b3ff29d10f7500fe41b3e959f68
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561080"
---
# Função JsCreateTypedArray
Cria um objeto matriz tipada JavaScript.  
  
## Sintaxe  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateTypedArray(  
   _In_ JsTypedArrayType arrayType,  
   _In_ JsValueRef baseArray,  
   _In_ unsigned int byteOffset,  
   _In_ unsigned int elementLength,  
   _Out_ JsValueRef *result  
);  
```  
  
#### Parâmetros  
 `arrayType`  
 O tipo da matriz a ser criada.  
  
 `baseArray`  
 A matriz base da nova matriz. Use `JS_INVALID_REFERENCE` se não houver matriz base.  
  
 `byteOffset`  
 O offset em bytes do início de `baseArray` ( `ArrayBuffer` ) para a matriz de resultado digitada para fazer referência. Aplicável somente quando `baseArray` é um `ArrayBuffer` objeto. Caso contrário, deve ser 0.  
  
 `elementLength`  
 O número de elementos na matriz. Só se aplica ao criar uma nova matriz tipada sem `baseArray` ( `baseArray` is `JS_INVALID_REFERENCE` ) ou quando `baseArray` é um `ArrayBuffer` objeto. Caso contrário, deve ser 0.  
  
 `result`  
 O novo objeto de matriz tipada.  
  
## Valor de retorno  
 O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.  
  
## Comentários  
 `baseArray`Pode ser uma `ArrayBuffer` , outra matriz tipada ou JavaScript `Array` . A matriz tipada retornada usará o `baseArray` se for um `ArrayBuffer` ou, caso contrário, criará e usará uma cópia da matriz de origem subjacente.  
  
 Requer um contexto de script ativo.  
  
 Essa API só tem suporte no modo Microsoft Edge.  
  
## Requisitos  
 **Header:** jsrt. h  
  
## Consulte também  
 [Referência (tempo de execução JavaScript)](../chakra-hosting/reference-javascript-runtime.md)