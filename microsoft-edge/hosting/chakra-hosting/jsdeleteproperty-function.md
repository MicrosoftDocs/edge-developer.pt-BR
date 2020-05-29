---
description: Exclui a propriedade de um objeto.
title: Função JsDeleteProperty | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsDeleteProperty
helpviewer_keywords:
- JsDeleteProperty function
ms.assetid: 0f6ac6a7-3576-42f5-98d0-1c06542c8149
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: c5539238324d59126b45f19fa9a6f8facc0f2ee3
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561073"
---
# <span data-ttu-id="9aadb-103">Função JsDeleteProperty</span><span class="sxs-lookup"><span data-stu-id="9aadb-103">JsDeleteProperty Function</span></span>
<span data-ttu-id="9aadb-104">Exclui a propriedade de um objeto.</span><span class="sxs-lookup"><span data-stu-id="9aadb-104">Deletes an object's property.</span></span>  
  
## <span data-ttu-id="9aadb-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9aadb-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsDeleteProperty(  
   _In_ JsValueRef object,  
   _In_ JsPropertyIdRef propertyId,  
   _In_ bool useStrictRules,  
   _Out_ JsValueRef *result  
);  
```  
  
#### <span data-ttu-id="9aadb-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9aadb-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="9aadb-107">O objeto que contém a propriedade.</span><span class="sxs-lookup"><span data-stu-id="9aadb-107">The object that contains the property.</span></span>  
  
 `propertyId`  
 <span data-ttu-id="9aadb-108">A ID da propriedade.</span><span class="sxs-lookup"><span data-stu-id="9aadb-108">The ID of the property.</span></span>  
  
 `useStrictRules`  
 <span data-ttu-id="9aadb-109">O conjunto de propriedades deve seguir as regras do modo estrito.</span><span class="sxs-lookup"><span data-stu-id="9aadb-109">The property set should follow strict mode rules.</span></span>  
  
 `result`  
 <span data-ttu-id="9aadb-110">Se a propriedade foi excluída.</span><span class="sxs-lookup"><span data-stu-id="9aadb-110">Whether the property was deleted.</span></span>  
  
## <span data-ttu-id="9aadb-111">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="9aadb-111">Return Value</span></span>  
 <span data-ttu-id="9aadb-112">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="9aadb-112">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="9aadb-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="9aadb-113">Remarks</span></span>  
 <span data-ttu-id="9aadb-114">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="9aadb-114">Requires an active script context.</span></span>  
  
## <span data-ttu-id="9aadb-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9aadb-115">Requirements</span></span>  
 <span data-ttu-id="9aadb-116">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="9aadb-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="9aadb-117">Consulte também</span><span class="sxs-lookup"><span data-stu-id="9aadb-117">See Also</span></span>  
 [<span data-ttu-id="9aadb-118">Referência (tempo de execução JavaScript)</span><span class="sxs-lookup"><span data-stu-id="9aadb-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)