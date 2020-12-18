---
description: Cria um valor JavaScript que é uma projeção da passada `VARIANT` .
title: Função JsVariantToValue | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsVariantToValue
helpviewer_keywords:
- JsVariantToValue function
ms.assetid: e8f9eb8b-55b3-4b65-927e-cad5b482edee
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 58c928b519b5a9a678b6cd6ad367e1db2332f021
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231571"
---
# Função JsVariantToValue

Cria um valor JavaScript que é uma projeção da passada `VARIANT` .  
  
## Sintaxe  
  
```cpp  
STDAPI_(JsErrorCode) JsVariantToValue(  
   _In_ VARIANT *variant,  
   _Out_ JsValueRef *value  
);  
```  
  
#### Parâmetros  
 `variant`  
 A `VARIANT` a a ser projetada.  
  
 `value`  
 Um valor JavaScript que é uma projeção de `VARIANT` .  
  
## Valor de retorno  
 O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.  
  
## Comentários  
 O valor projetado pode ser usado pelo script para chamar um objeto de automação COM do script. Os hosts são responsáveis por impor regras de Threading COM.  
  
 Requer um contexto de script ativo.  
  
## Requisitos  
 **Header:** jsrt. h  
  
## Consulte também  
 [Referência (Runtime do JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
