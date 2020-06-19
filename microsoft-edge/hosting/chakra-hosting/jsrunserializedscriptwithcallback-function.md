---
description: Executa um script serializado. Fornece a capacidade de carregar a fonte de script somente se/quando for necessária.
title: Função JsRunSerializedScriptWithCallback | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 0608d778-f65b-4dc5-a745-364aac57ef59
caps.latest.revision: 4
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 84a74d3c1aa68469dfe2fe42fdee685faa4c358c
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752217"
---
# Função JsRunSerializedScriptWithCallback
Executa um script serializado. Fornece a capacidade de carregar a fonte de script somente se/quando for necessária.  
  
## Sintaxe  
  
```cpp  
STDAPI_(JsErrorCode) JsRunSerializedScriptWithCallback(  
  _In_ JsSerializedScriptLoadSourceCallback scriptLoadCallback,  
  _In_ JsSerializedScriptUnloadCallback scriptUnloadCallback,  
  _In_ BYTE *buffer,  
  _In_ JsSourceContext sourceContext,  
  _In_z_ const wchar_t *sourceUrl,  
  _Out_opt_ JsValueRef *result  
);  
  
```  
  
#### Parâmetros  
 `scriptLoadCallback`  
 Retorno de chamada chamado quando o código-fonte do script precisa ser carregado.  
  
 `scriptUnloadCallback`  
 Retorno de chamada chamado quando o script serializado e o código-fonte não são mais necessários.  
  
 `buffer`  
 O script serializado.  
  
 `sourceContext`  
 Um cookie identificando o script que pode ser usado por contextos de script debuggable.     Esse contexto passará para scriptLoadCallback e scriptUnloadCallback.  
  
 `sourceUrl`  
 O local de onde o script veio.  
  
 `result`  
 O resultado da execução do script, se houver. Esse parâmetro pode ser nulo.  
  
## Valor de retorno  
 O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.  
  
## Comentários  
  
> [!NOTE]
>  Esta API ainda não está disponível para aplicativos da loja.  
  
 Requer um contexto de script ativo.  
  
 O tempo de execução será armazenado no buffer até que todas as instâncias criadas do buffer sejam coletadas como lixo.  Em seguida, ele chamará scriptUnloadCallback para informar ao chamador que é seguro liberar.  
  
## Requisitos  
 **Header:** jsrt. h  
  
## Consulte também  
 [Referência (Runtime do JavaScript)](../chakra-hosting/reference-javascript-runtime.md)