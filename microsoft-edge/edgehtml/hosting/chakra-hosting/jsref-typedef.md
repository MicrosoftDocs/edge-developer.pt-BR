---
description: Uma referência a um objeto pertencente ao coletor de lixo Chakra.
title: Typedef JsRef | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 6aafc39f-6b9c-457f-8bf0-48831bffe9b8
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 69d13472b15b5d448908b5dafb2e3d7dc0ace7e4
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231248"
---
# Typedef JsRef

Uma referência a um objeto pertencente ao coletor de lixo Chakra.  
  
## Sintaxe  
  
```cpp  
typedef void *JsRef;  
```  
  
## Comentários  
 Um tempo de execução do Chakra automaticamente controlará as referências do JsRef desde que elas estejam armazenadas em variáveis locais ou em parâmetros (ou seja, na pilha). Armazenar um JsRef em outro lugar diferente de na pilha requer chamar JsAddRef e JsRelease para gerenciar o tempo de vida do objeto, caso contrário, o coletor de lixo pode liberar o objeto enquanto ele ainda está em uso.  
  
## Requisitos  
 **Header:** jsrt. h  
  
## Consulte também  
 [Referência (Runtime do JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
