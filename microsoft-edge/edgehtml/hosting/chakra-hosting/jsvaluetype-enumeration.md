---
description: O tipo de JavaScript de um JsValueRef.
title: Enumeração JsValueType | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsValueType
helpviewer_keywords:
- JsValueType enumeration
ms.assetid: 6645e723-e554-41fc-b622-ab54ee044b3d
caps.latest.revision: 16
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 840afcde86d4df80490d463921a74c73e42ddfc2
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231572"
---
# <span data-ttu-id="12830-103">Enumeração JsValueType</span><span class="sxs-lookup"><span data-stu-id="12830-103">JsValueType Enumeration</span></span>

<span data-ttu-id="12830-104">O tipo de JavaScript de um JsValueRef.</span><span class="sxs-lookup"><span data-stu-id="12830-104">The JavaScript type of a JsValueRef.</span></span>  
  
## <span data-ttu-id="12830-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="12830-105">Syntax</span></span>  
  
```cpp  
enum JsValueType {  
    JsUndefined      = 0,  
    JsNull           = 1,  
    JsNumber         = 2,  
    JsString         = 3,  
    JsBoolean        = 4,  
    JsObject         = 5,  
    JsFunction       = 6,  
    JsError          = 7,  
    JsArray          = 8,  
    JsSymbol         = 9,  
    JsArrayBuffer    = 10,  
    JsTypedArray     = 11,  
    JsDataView       = 12,  
};  
```  
  
## <span data-ttu-id="12830-106">Parte</span><span class="sxs-lookup"><span data-stu-id="12830-106">Members</span></span>  
  
### <span data-ttu-id="12830-107">Valores</span><span class="sxs-lookup"><span data-stu-id="12830-107">Values</span></span>  
  
|<span data-ttu-id="12830-108">Nome</span><span class="sxs-lookup"><span data-stu-id="12830-108">Name</span></span>|<span data-ttu-id="12830-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="12830-109">Description</span></span>|  
|----------|-----------------|  
|`JsUndefined`|<span data-ttu-id="12830-110">O valor é o `undefined` valor.</span><span class="sxs-lookup"><span data-stu-id="12830-110">The value is the `undefined` value.</span></span>|  
|`JsNull`|<span data-ttu-id="12830-111">O valor é o `null` valor.</span><span class="sxs-lookup"><span data-stu-id="12830-111">The value is the `null` value.</span></span>|  
|`JsNumber`|<span data-ttu-id="12830-112">O valor é um valor de número JavaScript.</span><span class="sxs-lookup"><span data-stu-id="12830-112">The value is a JavaScript number value.</span></span>|  
|`JsString`|<span data-ttu-id="12830-113">O valor é um valor de cadeia de caracteres JavaScript.</span><span class="sxs-lookup"><span data-stu-id="12830-113">The value is a JavaScript string value.</span></span>|  
|`JsBoolean`|<span data-ttu-id="12830-114">O valor é um valor booliano de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="12830-114">The value is a JavaScript Boolean value.</span></span>|  
|`JsObject`|<span data-ttu-id="12830-115">O valor é um valor de objeto JavaScript.</span><span class="sxs-lookup"><span data-stu-id="12830-115">The value is a JavaScript object value.</span></span>|  
|`JsFunction`|<span data-ttu-id="12830-116">O valor é um valor de objeto function JavaScript.</span><span class="sxs-lookup"><span data-stu-id="12830-116">The value is a JavaScript function object value.</span></span>|  
|`JsError`|<span data-ttu-id="12830-117">O valor é um valor de objeto de erro JavaScript.</span><span class="sxs-lookup"><span data-stu-id="12830-117">The value is a JavaScript error object value.</span></span>|  
|`JsArray`|<span data-ttu-id="12830-118">O valor é um valor de objeto de matriz JavaScript.</span><span class="sxs-lookup"><span data-stu-id="12830-118">The value is a JavaScript array object value.</span></span>|  
|`JsSymbol`|<span data-ttu-id="12830-119">O valor é um valor de símbolo JavaScript.</span><span class="sxs-lookup"><span data-stu-id="12830-119">The value is a JavaScript symbol value.</span></span><br /><br /> <span data-ttu-id="12830-120">Esse valor de enumeração só tem suporte no modo Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="12830-120">This enumeration value is supported only in Microsoft Edge mode.</span></span>|  
|`JsArrayBuffer`|<span data-ttu-id="12830-121">O valor é um `ArrayBuffer` valor de objeto JavaScript.</span><span class="sxs-lookup"><span data-stu-id="12830-121">The value is a JavaScript `ArrayBuffer` object value.</span></span><br /><br /> <span data-ttu-id="12830-122">Esse valor de enumeração só tem suporte no modo Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="12830-122">This enumeration value is supported only in Microsoft Edge mode.</span></span>|  
|`JsTypedArray`|<span data-ttu-id="12830-123">O valor é um valor de objeto matriz tipada do JavaScript.</span><span class="sxs-lookup"><span data-stu-id="12830-123">The value is a JavaScript typed array object value.</span></span><br /><br /> <span data-ttu-id="12830-124">Esse valor de enumeração só tem suporte no modo Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="12830-124">This enumeration value is supported only in Microsoft Edge mode.</span></span>|  
|`JsDataView`|<span data-ttu-id="12830-125">O valor é um `DataView` valor de objeto JavaScript.</span><span class="sxs-lookup"><span data-stu-id="12830-125">The value is a JavaScript `DataView` object value.</span></span><br /><br /> <span data-ttu-id="12830-126">Esse valor de enumeração só tem suporte no modo Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="12830-126">This enumeration value is supported only in Microsoft Edge mode.</span></span>|  
  
## <span data-ttu-id="12830-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="12830-127">Requirements</span></span>  
 <span data-ttu-id="12830-128">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="12830-128">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="12830-129">Consulte também</span><span class="sxs-lookup"><span data-stu-id="12830-129">See Also</span></span>  
 [<span data-ttu-id="12830-130">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="12830-130">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
