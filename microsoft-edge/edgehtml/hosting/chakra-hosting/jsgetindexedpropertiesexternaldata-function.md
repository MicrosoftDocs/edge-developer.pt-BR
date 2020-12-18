---
description: Recupera as propriedades de dados externos de propriedades indexadas de um objeto.
title: Função JsGetIndexedPropertiesExternalData | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 2c313163-3462-42fd-8dee-3dfb3ac7f43f
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 627aaef48def2e042927467e1cbb6d6b7c06a525
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231254"
---
# Função JsGetIndexedPropertiesExternalData

Recupera as propriedades de dados externos de propriedades indexadas de um objeto.  
  
## Sintaxe  
  
```cpp  
STDAPI_(JsErrorCode) JsGetIndexedPropertiesExternalData(  
   _In_ JsValueRef object,  
   _Out_ void** data,  
   _Out_ JsTypedArrayType* arrayType,  
   _Out_ unsigned int* elementLength  
);  
```  
  
#### Parâmetros  
 `object`  
 O objeto.  
  
 `data`  
 O repositório de retorno de dados externos das propriedades indexadas do objeto.  
  
 `arrayType`  
 O tipo de elemento array em dados externos.  
  
 `elementLength`  
 O número de elementos de matriz em dados externos.  
  
## Valor de retorno  
 O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.  
  
## Comentários  
 Essa API só tem suporte no modo Microsoft Edge.  
  
## Requisitos  
 **Header:** jsrt. h  
  
## Consulte também  
 [Referência (Runtime do JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
