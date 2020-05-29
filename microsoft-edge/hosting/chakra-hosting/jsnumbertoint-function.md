---
description: Recupera o `int` valor de um valor numérico.
title: Função JsNumberToInt | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 8b9256d6-76ac-4c74-a97c-fbb16c13f5f5
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: cf4c8cb42c737cfb9efee5422fe6bb3c1389cbfd
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10562155"
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
 [Referência (tempo de execução JavaScript)](../chakra-hosting/reference-javascript-runtime.md)