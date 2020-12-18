---
description: Inicia a depuração no contexto atual.
title: Função JsStartDebugging | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsStartDebugging
helpviewer_keywords:
- JsStartDebugging function
ms.assetid: c48ba02d-6d47-466f-a970-02f087d525f3
caps.latest.revision: 15
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 9685779911db8e3045986682b66d13e38c70fe8d
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231917"
---
# Função JsStartDebugging

Inicia a depuração no contexto atual.  
  
## Sintaxe  
  
```cpp  
// Microsoft Edge mode signature  
STDAPI_(JsErrorCode) JsStartDebugging();  
  
// Legacy mode signature  
STDAPI_(JsErrorCode)  JsStartDebugging(  
   _In_ IDebugApplication *debugApplication  
);  
```  
  
#### Parâmetros  
 `debugApplication`  
 O aplicativo de depuração a ser usado para depuração.  
  
## Valor de retorno  
 O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.  
  
## Comentários  
 O host deve ter certeza de que `CoInitializeEx` é chamado com `COINIT_MULTITHREADED` ou `COINIT_APARTMENTTHREADED` pelo menos uma vez antes de usar essa API  
  
 `debugApplication`Não há suporte para o parâmetro no modo Microsoft Edge. Para obter mais informações sobre o uso dessa API no modo Microsoft Edge, consulte [direcionamento de mecanismos do Microsoft Edge versus herdados](../chakra-hosting/targeting-edge-vs-legacy-engines-in-jsrt-apis.md).  
  
## Requisitos  
 **Header:** jsrt. h  
  
## Consulte também  
 [Referência (Runtime do JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
