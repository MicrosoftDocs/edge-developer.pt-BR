---
description: Executa o `instanceof` teste de operador JavaScript.
title: Função JsInstanceOf | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 94399a62-b996-4fd2-82ce-1c26e7a4da08
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 4d9bf2e4c3da9f83fdf7c0ef4e2c31df04670420
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/18/2020
ms.locfileid: "10751972"
---
# Função JsInstanceOf
Executa o `instanceof` teste de operador JavaScript.  
  
## Sintaxe  
  
```cpp  
JsInstanceOf(   
  _In_ JsValueRef object,  
  _In_ JsValueRef constructor,  
  _Out_ bool *result  
);  
  
```  
  
#### Parâmetros  
 `object`  
 O objeto a ser testado.  
  
 `constructor`  
 A função do Construtor a ser testada.  
  
 `result`  
 Se o "Construtor do objeto instanceof" é verdadeiro.  
  
## Valor de retorno  
 O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.  
  
## Comentários  
 Requer um contexto de script ativo.  
  
## Requisitos  
 **Header:** jsrt. h  
  
## Consulte também  
 [Referência (Runtime do JavaScript)](../chakra-hosting/reference-javascript-runtime.md)