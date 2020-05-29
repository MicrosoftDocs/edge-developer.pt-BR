---
description: Obtém o tipo de propriedade.
title: Função JsGetPropertyIdType | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 2b6e85ad-c630-4a07-a759-3b344d06faaa
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: a43cfc2efd69cc14813ad88850afbf602d477d71
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10562177"
---
# <span data-ttu-id="81cf7-103">Função JsGetPropertyIdType</span><span class="sxs-lookup"><span data-stu-id="81cf7-103">JsGetPropertyIdType Function</span></span>
<span data-ttu-id="81cf7-104">Obtém o tipo de propriedade.</span><span class="sxs-lookup"><span data-stu-id="81cf7-104">Gets the type of property.</span></span>  
  
## <span data-ttu-id="81cf7-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="81cf7-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetPropertyIdType(  
   _In_ JsPropertyIdRef propertyId,  
   _Out_ JsPropertyIdType* propertyIdType  
);  
```  
  
#### <span data-ttu-id="81cf7-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="81cf7-106">Parameters</span></span>  
 `propertyId`  
 <span data-ttu-id="81cf7-107">A ID da propriedade para obter o tipo.</span><span class="sxs-lookup"><span data-stu-id="81cf7-107">The property ID to get the type of.</span></span>  
  
 `propertyIdType`  
 <span data-ttu-id="81cf7-108">A `JsPropertyIdType` ID da propriedade fornecida.</span><span class="sxs-lookup"><span data-stu-id="81cf7-108">The `JsPropertyIdType` of the given property ID.</span></span>  
  
## <span data-ttu-id="81cf7-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="81cf7-109">Return Value</span></span>  
 <span data-ttu-id="81cf7-110">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="81cf7-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="81cf7-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="81cf7-111">Remarks</span></span>  
 <span data-ttu-id="81cf7-112">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="81cf7-112">Requires an active script context.</span></span>  
  
 <span data-ttu-id="81cf7-113">Essa API só tem suporte no modo Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="81cf7-113">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="81cf7-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="81cf7-114">Requirements</span></span>  
 <span data-ttu-id="81cf7-115">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="81cf7-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="81cf7-116">Consulte também</span><span class="sxs-lookup"><span data-stu-id="81cf7-116">See Also</span></span>  
 [<span data-ttu-id="81cf7-117">Referência (tempo de execução JavaScript)</span><span class="sxs-lookup"><span data-stu-id="81cf7-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)