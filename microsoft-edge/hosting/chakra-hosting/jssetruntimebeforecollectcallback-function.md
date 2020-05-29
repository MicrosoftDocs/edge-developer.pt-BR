---
description: 'Define uma função de retorno de chamada que é chamada pelo tempo de execução antes da coleta de lixo. '
title: Função JsSetRuntimeBeforeCollectCallback | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsSetRuntimeBeforeCollectCallback
helpviewer_keywords:
- JsSetRuntimeBeforeCollectCallback function
ms.assetid: 7b2fb911-6007-4ed9-a307-66cefe590ea4
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 31aefd28698c14a6fe17421a990a7c8b120876bf
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10562008"
---
# Função JsSetRuntimeBeforeCollectCallback
Define uma função de retorno de chamada que é chamada pelo tempo de execução antes da coleta de lixo.  
  
## Sintaxe  
  
```cpp  
STDAPI_(JsErrorCode) JsSetRuntimeBeforeCollectCallback(  
   _In_ JsRuntimeHandle runtime,  
   _In_opt_ void *callbackState,  
   _In_ JsBeforeCollectCallback beforeCollectCallback  
);  
```  
  
#### Parâmetros  
 `runtime`  
 O tempo de execução para o qual registrar o retorno de chamada de alocação.  
  
 `callbackState`  
 Estado fornecido pelo usuário que será devolvido ao retorno de chamada.  
  
 `beforeCollectCallback`  
 A função de retorno de chamada sendo definida.  
  
## Valor de retorno  
 O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.  
  
## Comentários  
 O retorno de chamada é invocado no thread de execução do tempo de execução atual, portanto a execução é bloqueada até que o retorno de chamada seja concluído.  
  
 O retorno de chamada pode ser usado pelos hosts para se preparar para a coleta de lixo. Por exemplo, ao liberar referências desnecessárias em objetos Chakra.  
  
## Requisitos  
 **Header:** jsrt. h  
  
## Consulte também  
 [Referência (tempo de execução JavaScript)](../chakra-hosting/reference-javascript-runtime.md)