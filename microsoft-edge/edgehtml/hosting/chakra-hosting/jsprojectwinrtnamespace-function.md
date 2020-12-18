---
description: Projetar um namespace WinRT.
title: Função JsProjectWinRTNamespace | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 8a23c154-df4b-4ce3-9fef-f41f90acdb87
caps.latest.revision: 5
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: f781cf90aaec68b2bd305bf34c453fc663ad0187
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231989"
---
# Função JsProjectWinRTNamespace

Projetar um namespace WinRT.  
  
## Sintaxe  
  
```cpp  
STDAPI_(JsErrorCode)  
   JsProjectWinRTNamespace(  
   _In_z_ const wchar_t *namespaceName  
);  
```  
  
#### Parâmetros  
 `namespaceName`  
 O namespace WinRT seja projetado.  
  
## Valor de retorno  
 O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.  
  
## Comentários  
 Requer um contexto de script ativo.  
  
 Essa API só tem suporte no modo EdgeHTML.  
  
> [!NOTE]
>  O WinRT foi o nome da plataforma antes da plataforma universal do Windows (UWP).  
  
## Requisitos  
 **Header:** jsrt. h  
  
## Consulte também  
 [Referência (Runtime do JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
