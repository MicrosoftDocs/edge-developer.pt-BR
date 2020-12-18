---
description: Cria um valor JavaScript que é uma projeção do ponteiro passado `IInspectable` .
title: Função JsInspectableToObject | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: dd0ad567-2ba8-4a63-bee4-2c6ff5ce9fa9
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: a5d3d91b38c9db5de2eb8fb02526f6072f0f5147
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231806"
---
# Função JsInspectableToObject

Cria um valor JavaScript que é uma projeção do ponteiro passado `IInspectable` .  
  
## Sintaxe  
  
```cpp  
STDAPI_(JsErrorCode) JsInspectableToObject(  
        _In_ IInspectable  *inspectable,  
        _Out_ JsValueRef *value  
);  
```  
  
#### Parâmetros  
 `inspectable`  
 A `IInspectable` a a ser projetada.  
  
 `value`  
 Um valor JavaScript que é uma projeção de `IInspectable` .  
  
## Valor de retorno  
 O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.  
  
## Comentários  
 O valor projetado pode ser usado pelo script para chamar um objeto WinRT. Os hosts são responsáveis por impor regras de Threading COM.  
  
 Requer um contexto de script ativo.  
  
 Essa API só tem suporte no modo EdgeHTML.  
  
## Requisitos  
 **Header:** jsrt. h  
  
## Consulte também  
 [Referência (Runtime do JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
