---
description: O tipo de JavaScript de um JsValueRef.
title: Enumeração JsValueType | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsValueType
helpviewer_keywords:
- JsValueType enumeration
ms.assetid: 6645e723-e554-41fc-b622-ab54ee044b3d
caps.latest.revision: 16
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: c42231525b55b49f0931a2ace33b373e0d4ae441
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10560993"
---
# <span data-ttu-id="1ba7f-103">Enumeração JsValueType</span><span class="sxs-lookup"><span data-stu-id="1ba7f-103">JsValueType Enumeration</span></span>
<span data-ttu-id="1ba7f-104">O tipo de JavaScript de um JsValueRef.</span><span class="sxs-lookup"><span data-stu-id="1ba7f-104">The JavaScript type of a JsValueRef.</span></span>  
  
## <span data-ttu-id="1ba7f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1ba7f-105">Syntax</span></span>  
  
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
  
## <span data-ttu-id="1ba7f-106">Parte</span><span class="sxs-lookup"><span data-stu-id="1ba7f-106">Members</span></span>  
  
### <span data-ttu-id="1ba7f-107">Valores</span><span class="sxs-lookup"><span data-stu-id="1ba7f-107">Values</span></span>  
  
|<span data-ttu-id="1ba7f-108">Nome</span><span class="sxs-lookup"><span data-stu-id="1ba7f-108">Name</span></span>|<span data-ttu-id="1ba7f-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="1ba7f-109">Description</span></span>|  
|----------|-----------------|  
|`JsUndefined`|<span data-ttu-id="1ba7f-110">O valor é o `undefined` valor.</span><span class="sxs-lookup"><span data-stu-id="1ba7f-110">The value is the `undefined` value.</span></span>|  
|`JsNull`|<span data-ttu-id="1ba7f-111">O valor é o `null` valor.</span><span class="sxs-lookup"><span data-stu-id="1ba7f-111">The value is the `null` value.</span></span>|  
|`JsNumber`|<span data-ttu-id="1ba7f-112">O valor é um valor de número JavaScript.</span><span class="sxs-lookup"><span data-stu-id="1ba7f-112">The value is a JavaScript number value.</span></span>|  
|`JsString`|<span data-ttu-id="1ba7f-113">O valor é um valor de cadeia de caracteres JavaScript.</span><span class="sxs-lookup"><span data-stu-id="1ba7f-113">The value is a JavaScript string value.</span></span>|  
|`JsBoolean`|<span data-ttu-id="1ba7f-114">O valor é um valor booliano de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="1ba7f-114">The value is a JavaScript Boolean value.</span></span>|  
|`JsObject`|<span data-ttu-id="1ba7f-115">O valor é um valor de objeto JavaScript.</span><span class="sxs-lookup"><span data-stu-id="1ba7f-115">The value is a JavaScript object value.</span></span>|  
|`JsFunction`|<span data-ttu-id="1ba7f-116">O valor é um valor de objeto function JavaScript.</span><span class="sxs-lookup"><span data-stu-id="1ba7f-116">The value is a JavaScript function object value.</span></span>|  
|`JsError`|<span data-ttu-id="1ba7f-117">O valor é um valor de objeto de erro JavaScript.</span><span class="sxs-lookup"><span data-stu-id="1ba7f-117">The value is a JavaScript error object value.</span></span>|  
|`JsArray`|<span data-ttu-id="1ba7f-118">O valor é um valor de objeto de matriz JavaScript.</span><span class="sxs-lookup"><span data-stu-id="1ba7f-118">The value is a JavaScript array object value.</span></span>|  
|`JsSymbol`|<span data-ttu-id="1ba7f-119">O valor é um valor de símbolo JavaScript.</span><span class="sxs-lookup"><span data-stu-id="1ba7f-119">The value is a JavaScript symbol value.</span></span><br /><br /> <span data-ttu-id="1ba7f-120">Esse valor de enumeração só tem suporte no modo Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="1ba7f-120">This enumeration value is supported only in Microsoft Edge mode.</span></span>|  
|`JsArrayBuffer`|<span data-ttu-id="1ba7f-121">O valor é um `ArrayBuffer` valor de objeto JavaScript.</span><span class="sxs-lookup"><span data-stu-id="1ba7f-121">The value is a JavaScript `ArrayBuffer` object value.</span></span><br /><br /> <span data-ttu-id="1ba7f-122">Esse valor de enumeração só tem suporte no modo Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="1ba7f-122">This enumeration value is supported only in Microsoft Edge mode.</span></span>|  
|`JsTypedArray`|<span data-ttu-id="1ba7f-123">O valor é um valor de objeto matriz tipada do JavaScript.</span><span class="sxs-lookup"><span data-stu-id="1ba7f-123">The value is a JavaScript typed array object value.</span></span><br /><br /> <span data-ttu-id="1ba7f-124">Esse valor de enumeração só tem suporte no modo Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="1ba7f-124">This enumeration value is supported only in Microsoft Edge mode.</span></span>|  
|`JsDataView`|<span data-ttu-id="1ba7f-125">O valor é um `DataView` valor de objeto JavaScript.</span><span class="sxs-lookup"><span data-stu-id="1ba7f-125">The value is a JavaScript `DataView` object value.</span></span><br /><br /> <span data-ttu-id="1ba7f-126">Esse valor de enumeração só tem suporte no modo Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="1ba7f-126">This enumeration value is supported only in Microsoft Edge mode.</span></span>|  
  
## <span data-ttu-id="1ba7f-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1ba7f-127">Requirements</span></span>  
 <span data-ttu-id="1ba7f-128">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="1ba7f-128">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="1ba7f-129">Consulte também</span><span class="sxs-lookup"><span data-stu-id="1ba7f-129">See Also</span></span>  
 [<span data-ttu-id="1ba7f-130">Referência (tempo de execução JavaScript)</span><span class="sxs-lookup"><span data-stu-id="1ba7f-130">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)