---
description: Informa o tempo de execução para fazer qualquer processamento de ociosidade necessário.
title: Função JsIdle | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsIdle
helpviewer_keywords:
- JsIdle function
ms.assetid: 372d1c62-8e19-4886-aa33-364cabc09bba
caps.latest.revision: 13
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: ecba0aafb6b4dcccb4485c2956cae5ce4045355f
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231935"
---
# Função JsIdle

Informa o tempo de execução para fazer qualquer processamento de ociosidade necessário.  
  
## Sintaxe  
  
```cpp  
STDAPI_(JsErrorCode) JsIdle(  
   _Out_opt_ unsigned int *nextIdleTick  
);  
```  
  
#### Parâmetros  
 `nextIdleTick`  
 O próximo tique do sistema quando houver mais trabalho ocioso a fazer. Pode ser nulo. Retorna o número máximo de tiques se não houver nenhum trabalho ocioso futuro.  
  
## Valor de retorno  
 O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.  
  
## Comentários  
 Se o processamento de ociosidade tiver sido habilitado para o tempo de execução atual, a chamada `JsIdle` informará o tempo de execução atual que o host está ocioso e que o tempo de execução pode executar tarefas de limpeza de memória.  
  
 `JsIdle` também pode retornar o número de tiques do sistema até que haja mais trabalho ocioso para o tempo de execução. Chamar `JsIdle` antes deste número de tiques aprovados não funcionará.  
  
 Requer um contexto de script ativo.  
  
## Requisitos  
 **Header:** jsrt. h  
  
## Consulte também  
 [Referência (Runtime do JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
