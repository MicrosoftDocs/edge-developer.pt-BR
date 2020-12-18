---
description: Recupera o `int` valor de um valor numérico.
title: Função JsNumberToInt | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 8b9256d6-76ac-4c74-a97c-fbb16c13f5f5
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 928be9a7cc5cd3e26e8b8df99af1e08a6c50209c
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231763"
---
# Função JsNumberToInt

Recupera o `int` valor de um valor numérico.  
  
## Sintaxe  
  
```cpp  
STDAPI_(JsErrorCode) JsNumberToInt(  
      _In_ JsValueRef value,  
      _Out_ int *intValue  
);  
```  
  
#### Parâmetros  
 `value`  
 O valor numérico a ser convertido em um `int` valor.  
  
 `intValue`  
 O `int` valor.  
  
## Valor de retorno  
  
## Comentários  
 Essa função recupera o valor de um valor numérico e converte para um `int` valor. Ocorrerá uma falha `JsErrorInvalidArgument` se o tipo do valor não for número.  
  
 Requer um contexto de script ativo.  
  
 Essa API só tem suporte no modo EdgeHTML.  
  
## Requisitos  
 **Header:** jsrt. h  
  
## Consulte também  
 [Referência (Runtime do JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
