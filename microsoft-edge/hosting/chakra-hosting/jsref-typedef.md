---
description: Uma referência a um objeto pertencente ao coletor de lixo Chakra.
title: Typedef JsRef | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 6aafc39f-6b9c-457f-8bf0-48831bffe9b8
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: f5ce1ada67a4530ba57345b90c0b7deba6954c7c
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10562139"
---
# <span data-ttu-id="58575-103">Typedef JsRef</span><span class="sxs-lookup"><span data-stu-id="58575-103">JsRef Typedef</span></span>
<span data-ttu-id="58575-104">Uma referência a um objeto pertencente ao coletor de lixo Chakra.</span><span class="sxs-lookup"><span data-stu-id="58575-104">A reference to an object owned by the Chakra garbage collector.</span></span>  
  
## <span data-ttu-id="58575-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="58575-105">Syntax</span></span>  
  
```cpp  
typedef void *JsRef;  
```  
  
## <span data-ttu-id="58575-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="58575-106">Remarks</span></span>  
 <span data-ttu-id="58575-107">Um tempo de execução do Chakra automaticamente controlará as referências do JsRef desde que elas estejam armazenadas em variáveis locais ou em parâmetros (ou seja, na pilha).</span><span class="sxs-lookup"><span data-stu-id="58575-107">A Chakra runtime will automatically track JsRef references as long as they are on stored in local variables or in parameters (i.e. on the stack).</span></span> <span data-ttu-id="58575-108">Armazenar um JsRef em outro lugar diferente de na pilha requer chamar JsAddRef e JsRelease para gerenciar o tempo de vida do objeto, caso contrário, o coletor de lixo pode liberar o objeto enquanto ele ainda está em uso.</span><span class="sxs-lookup"><span data-stu-id="58575-108">Storing a JsRef somewhere other than on the stack requires calling JsAddRef and JsRelease to manage the lifetime of the object, otherwise the garbage collector may free the object while it is still in use.</span></span>  
  
## <span data-ttu-id="58575-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="58575-109">Requirements</span></span>  
 <span data-ttu-id="58575-110">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="58575-110">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="58575-111">Consulte também</span><span class="sxs-lookup"><span data-stu-id="58575-111">See Also</span></span>  
 [<span data-ttu-id="58575-112">Referência (tempo de execução JavaScript)</span><span class="sxs-lookup"><span data-stu-id="58575-112">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)