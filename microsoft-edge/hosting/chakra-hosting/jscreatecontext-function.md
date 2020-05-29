---
description: Cria um contexto de script para executar scripts.
title: Função JsCreateContext | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsCreateContext
helpviewer_keywords:
- JsCreateContext function
ms.assetid: aceca043-2c73-4029-a06c-8ad6695109cf
caps.latest.revision: 15
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 06bd4c4780a8c7610ebc95cfc0da058306ce5b78
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561108"
---
# Função JsCreateContext
Cria um contexto de script para executar scripts.  
  
## Sintaxe  
  
```cpp  
// Microsoft Edge mode signature  
STDAPI_(JsErrorCode) JsCreateContext(  
   _In_ JsRuntimeHandle runtime,  
   _Out_ JsContextRef *newContext);  
  
// Legacy mode signature  
STDAPI_(JsErrorCode) JsCreateContext(  
   _In_ JsRuntimeHandle runtime,  
   _In_ IDebugApplication *debugApplication,  
   _Out_ JsContextRef *newContext  
);  
```  
  
#### Parâmetros  
 `runtime`  
 O tempo de execução em que o contexto do script está sendo criado.  
  
 `debugApplication`  
 O aplicativo de depuração a ser usado para depuração. Esse parâmetro pode ser nulo e, nesse caso, a depuração não está habilitada para o contexto.  
  
 `newContext`  
 O contexto de script criado.  
  
## Valor de retorno  
 O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.  
  
## Comentários  
 Cada contexto de script tem seu próprio objeto global que é isolado de todos os outros contextos de script.  
  
 `debugApplication`Não há suporte para o parâmetro no modo Microsoft Edge. Para obter mais informações sobre o uso dessa API no modo Microsoft Edge, consulte [direcionamento de mecanismos do Microsoft Edge versus herdados](../chakra-hosting/targeting-edge-vs-legacy-engines-in-jsrt-apis.md).  
  
## Requisitos  
 **Header:** jsrt. h  
  
## Consulte também  
 [Referência (tempo de execução JavaScript)](../chakra-hosting/reference-javascript-runtime.md)