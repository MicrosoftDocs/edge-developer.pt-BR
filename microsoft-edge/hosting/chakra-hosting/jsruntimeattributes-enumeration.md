---
description: 'Atributos de um tempo de execução. '
title: Enumeração JsRuntimeAttributes | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsRuntimeAttributes
helpviewer_keywords:
- JsRuntimeAttributes enumeration
ms.assetid: f76d82e9-a695-4d6a-96c1-b3a4d27fed68
caps.latest.revision: 14
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 9b8f6788f1de4988e3936701cfc742a564c92cfd
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10562124"
---
# Enumeração JsRuntimeAttributes
Atributos de um tempo de execução.  
  
## Sintaxe  
  
```cpp  
enum JsRuntimeAttributes;  
```  
  
## Parte  
  
### Valores  
  
|Nome|Descrição|  
|----------|-----------------|  
|`JsRuntimeAttributeAllowScriptInterrupt`|O tempo de execução deve dar suporte à interrupção de script confiável. Isso aumenta o número de locais em que o tempo de execução verifica se há solicitações de interrupção de script ao custo de uma pequena quantidade de desempenho de tempo de execução.|  
|`JsRuntimeAttributeDisableBackgroundWork`|O tempo de execução não fará qualquer trabalho (como a coleta de lixo) em threads em segundo plano.|  
|`JsRuntimeAttributeDisableEval`|O uso do `eval` `function` Construtor ou gerará uma exceção.|  
|`JsRuntimeAttributeDisableNativeCodeGeneration`|O tempo de execução não irá gerar código nativo.|  
|`JsRuntimeAttributeEnableExperimentalFeatures`|O tempo de execução habilitará todos os recursos experimentais.|  
|`JsRuntimeAttributeEnableIdleProcessing`|O host chamará `JsIdle` , portanto, habilitar o processamento de ociosidade. Caso contrário, o tempo de execução gerenciará a memória de forma ligeiramente mais agressiva.|  
|`JsRuntimeAttributeDispatchSetExceptionsToDebugger`|A chamada `JsSetException` também enviará a exceção para o depurador de script (se houver) dando ao depurador uma chance de interromper a exceção.|  
|`JsRuntimeAttributeNone`|Nenhum atributo especial.|  
  
## Requisitos  
 **Header:** jsrt. h  
  
## Consulte também  
 [Referência (tempo de execução JavaScript)](../chakra-hosting/reference-javascript-runtime.md)