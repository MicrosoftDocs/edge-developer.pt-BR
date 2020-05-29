---
description: Define as propriedades indexadas de um objeto para dados externos. Os dados externos serão usados como loja de volta para as propriedades indexadas do objeto e acessados como uma matriz digitada.
title: Função JsSetIndexedPropertiesToExternalData | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: cee2d86d-ed42-4acb-86ef-95a67e63d0d6
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: c1aed6e194b1dc1c35f403626a7b6c02a7752ffb
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10562108"
---
# Função JsSetIndexedPropertiesToExternalData
Define as propriedades indexadas de um objeto para dados externos. Os dados externos serão usados como loja de volta para as propriedades indexadas do objeto e acessados como uma matriz digitada.  
  
## Sintaxe  
  
```cpp  
STDAPI_(JsErrorCode) JsSetIndexedPropertiesToExternalData(  
   _In_ JsValueRef object,  
   _In_ void* data,  
   _In_ JsTypedArrayType arrayType,  
   _In_ unsigned int elementLength  
);  
```  
  
#### Parâmetros  
 `object`  
 O objeto no qual operar.  
  
 `data`  
 Os dados externos a serem usados como loja de volta para as propriedades indexadas do objeto.  
  
 `arrayType`  
 O tipo de elemento array em dados externos.  
  
 `elementLength`  
 O número de elementos de matriz em dados externos.  
  
## Valor de retorno  
 O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.  
  
## Comentários  
 Requer um contexto de script ativo.  
  
 Essa API só tem suporte no modo EdgeHTML.  
  
## Requisitos  
 **Header:** jsrt. h  
  
## Consulte também  
 [Referência (tempo de execução JavaScript)](../chakra-hosting/reference-javascript-runtime.md)