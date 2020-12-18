---
description: Interrompe a criação de perfil no contexto atual.
title: Função JsStopProfiling | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsStopProfiling
helpviewer_keywords:
- JsStopProfiling function
ms.assetid: 3639c04f-a0f9-418b-be39-92f64b4e7ef8
caps.latest.revision: 13
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 02c42afda7e61d71b90a9a1a71aa71cc53584ff8
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231615"
---
# Função JsStopProfiling

Interrompe a criação de perfil no contexto atual.  
  
## Sintaxe  
  
```cpp  
STDAPI_(JsErrorCode) JsStopProfiling(  
   _In_ HRESULT reason  
);  
```  
  
#### Parâmetros  
 `reason`  
 O motivo para interromper a criação de perfil para passar para o retorno de chamada do gerador de perfil.  
  
## Valor de retorno  
 O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.  
  
## Comentários  
 Não retornará um erro se o profiling não tiver começado.  
  
 Requer um contexto de script ativo.  
  
 Essa API tem suporte em aplicativos de área de trabalho, mas não é compatível com aplicativos da loja.  
  
## Requisitos  
 **Header:** jsrt. h  
  
## Consulte também  
 [Referência (Runtime do JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
