---
description: Um código de erro retornado de uma API de hospedagem Chakra.
title: Enumeração JsErrorCode | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsErrorCode
helpviewer_keywords:
- JsErrorCode enumeration
ms.assetid: 4902f3f3-47a5-4e74-9c29-f96eeecbcda9
caps.latest.revision: 15
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: b0a4aa7b47070bd5c8c7fe48cdbecf0dbefa9aa5
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231560"
---
# Enumeração JsErrorCode

Um código de erro retornado de uma API de hospedagem Chakra.  
  
## Sintaxe  
  
```cpp  
enum JsErrorCode : unsigned int;  
```  
  
## Parte  
  
### Valores  
  
|Nome|Descrição|  
|----------|-----------------|  
|`JsErrorAlreadyDebuggingContext`|O contexto não pode ser colocado em um estado de depuração porque já está em um estado de depuração.|  
|`JsErrorAlreadyProfilingContext`|O contexto não pode iniciar a criação de perfil porque já está criando o perfil.|  
|`JsErrorArgumentNotObject`|Uma API de hospedagem que opera em valores de objeto foi chamada com um valor não objeto.|  
|`JsErrorBadSerializedScript`|Um script serializado incorreto foi usado ou o script serializado foi serializado por uma versão diferente do mecanismo Chakra.|  
|`JsErrorCannotDisableExecution`|O tempo de execução não dá suporte à interrupção de script confiável.|  
|`JsErrorCannotSerializeDebugScript`|Scripts não podem ser serializados em contextos de depuração.|  
|`JsErrorCategoryEngine`|Categoria de erros relacionados a erros que ocorrem dentro do próprio mecanismo.|  
|`JsErrorCategoryFatal`|Categoria de erros que são fatais e significam falha do mecanismo.|  
|`JsErrorCategoryScript`|Categoria de erros relacionados a erros em um script.|  
|`JsErrorCategoryUsage`|Categoria de erros relacionados ao uso incorreto da própria API.|  
|`JsErrorFatal`|Ocorreu um erro fatal no mecanismo.|  
|`JsErrorHeapEnumInProgress`|No momento, uma enumeração de heap está em andamento no contexto do script.|  
|`JsErrorIdleNotEnabled`|Notificação ociosa fornecida quando o host não habilitou o processamento de ociosidade.|  
|`JsErrorInDisabledState`|O tempo de execução está em um estado desabilitado.|  
|`JsErrorInExceptionState`|O mecanismo está em um estado de exceção e nenhuma API pode ser chamada até que a exceção seja desmarcada.|  
|`JsErrorInObjectBeforeCollectCallback`|Não há suporte para a operação em um objeto antes da coleta de retorno de chamada.<br /><br /> Esse valor de enumeração só tem suporte no modo Microsoft Edge.|  
|`JsErrorInProfileCallback`|Um contexto de script está no meio de um retorno de chamada de perfil.|  
|`JsErrorInThreadServiceCallback`|No momento, um retorno de chamada de serviço de thread está em andamento.|  
|`JsErrorInvalidArgument`|Um argumento para uma API de hospedagem era inválido.|  
|`JsErrorNoCurrentContext`|A API de hospedagem requer que um contexto seja atual, mas não há contexto atual.|  
|`JsErrorNotImplemented`|Uma API de hospedagem ainda não foi implementada.|  
|`JsErrorNullArgument`|Um argumento para uma API de hospedagem era nulo em um contexto em que NULL não é permitido.|  
|`JsErrorObjectNotInspectable`|O objeto não pode ser quebrado para `IInspectable` ponteiro.<br /><br /> Esse valor de enumeração só tem suporte no modo Microsoft Edge.|  
|`JsErrorOutOfMemory`|O mecanismo Chakra não tem memória suficiente.|  
|`JsErrorPropertyNotSymbol`|Uma API de hospedagem que opera em IDs de propriedade de símbolo, mas foi chamada com uma ID de propriedade sem símbolo. O código de erro é retornado `JsGetSymbolFromPropertyId` se a função for chamada com a ID de propriedade sem símbolo.<br /><br /> Esse valor de enumeração só tem suporte no modo Microsoft Edge.|  
|`JsErrorPropertyNotString`|Uma API de hospedagem que opera em IDs de propriedades de cadeias de caracteres, mas foi chamada com uma ID de propriedade não cadeia de caracteres. O código de erro é retornado por existente `JsGetPropertyNamefromId` se a função for chamada com a ID de propriedade não cadeia de caracteres.<br /><br /> Esse valor de enumeração só tem suporte no modo Microsoft Edge.|  
|`JsErrorRuntimeInUse`|Não é possível descartar um tempo de execução que ainda está em uso.|  
|`JsErrorScriptCompile`|Falha na compilação do JavaScript.|  
|`JsErrorScriptEvalDisabled`|Um script foi encerrado porque tentou usar `eval` ou `function` eval foi desabilitada.|  
|`JsErrorScriptException`|Ocorreu uma exceção JavaScript ao executar um script.|  
|`JsErrorScriptTerminated`|Um script foi encerrado devido a uma solicitação para suspender um tempo de execução.|  
|`JsErrorWrongRuntime`|Uma API de hospedagem era chamada com objeto criado em um tempo de execução JavaScript diferente.|  
|`JsErrorWrongThread`|Uma API de hospedagem foi chamada no thread errado.|  
|`JsNoError`|Código de erro de sucesso.|  
  
## Requisitos  
 **Header:** jsrt. h  
  
## Consulte também  
 [Referência (Runtime do JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
