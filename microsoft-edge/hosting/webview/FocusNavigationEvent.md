---
description: O objeto despachado de um evento Focus que contém o motivo e a localização da navegação
title: Objeto FocusNavigationEvent
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2018
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, aplicativos do Windows 10, UWP, Edge
ms.openlocfilehash: b988bcd7ff252b9972bef9a31339a34b4b58d9ee
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10560976"
---
# <span data-ttu-id="0eefa-104">Objeto FocusNavigationEvent</span><span class="sxs-lookup"><span data-stu-id="0eefa-104">FocusNavigationEvent object</span></span>

<span data-ttu-id="0eefa-105">O objeto despachado da [**NavigateFocus**](../webview.md#navigatefocus) / [**DepartingFocus**](../webview.md#departingfocus) que contém o [**NavigationReason**](#navigationreason) e o local.</span><span class="sxs-lookup"><span data-stu-id="0eefa-105">The dispatched object from [**NavigateFocus**](../webview.md#navigatefocus)/[**DepartingFocus**](../webview.md#departingfocus) containing the [**NavigationReason**](#navigationreason) and location.</span></span> 

## <span data-ttu-id="0eefa-106">Métodos</span><span class="sxs-lookup"><span data-stu-id="0eefa-106">Methods</span></span>

### <span data-ttu-id="0eefa-107">requestFocus</span><span class="sxs-lookup"><span data-stu-id="0eefa-107">requestFocus</span></span>

<span data-ttu-id="0eefa-108">Chamado para mover o foco do aplicativo para o WebView.</span><span class="sxs-lookup"><span data-stu-id="0eefa-108">Called to move focus from the app to the webview.</span></span>

### <span data-ttu-id="0eefa-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0eefa-109">Parameters</span></span>

<span data-ttu-id="0eefa-110">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="0eefa-110">This method does not have parameters.</span></span>

### <span data-ttu-id="0eefa-111">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="0eefa-111">Return value</span></span>

<span data-ttu-id="0eefa-112">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="0eefa-112">This method does not return a value.</span></span>

## <span data-ttu-id="0eefa-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0eefa-113">Properties</span></span>
    
### <span data-ttu-id="0eefa-114">navigationReason</span><span class="sxs-lookup"><span data-stu-id="0eefa-114">navigationReason</span></span>

<span data-ttu-id="0eefa-115">O tipo enumerado **NavigationReason**, "Left", "up", "Right" ou "Down".</span><span class="sxs-lookup"><span data-stu-id="0eefa-115">Enumerated type **NavigationReason**, either "left", "up", "right", or "down".</span></span> 

<span data-ttu-id="0eefa-116">Essa propriedade é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="0eefa-116">This property is read-only.</span></span>

```js
var navigationReason = FocusNavigationEvent.navigationReason;
```

#### <span data-ttu-id="0eefa-117">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="0eefa-117">Property value</span></span>
<span data-ttu-id="0eefa-118">Tipo: **NavigationReason**</span><span class="sxs-lookup"><span data-stu-id="0eefa-118">Type: **NavigationReason**</span></span>

### <span data-ttu-id="0eefa-119">originHeight</span><span class="sxs-lookup"><span data-stu-id="0eefa-119">originHeight</span></span>

<span data-ttu-id="0eefa-120">O local da altura da origem do elemento a receber o foco.</span><span class="sxs-lookup"><span data-stu-id="0eefa-120">The origin height location of the element to be given focus.</span></span>

<span data-ttu-id="0eefa-121">Essa propriedade é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="0eefa-121">This property is read-only.</span></span>

```js
var originWoriginHeightidth = FocusNavigationEvent.originHeight;
```

#### <span data-ttu-id="0eefa-122">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="0eefa-122">Property value</span></span>
<span data-ttu-id="0eefa-123">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="0eefa-123">Type: **float**</span></span>

### <span data-ttu-id="0eefa-124">originLeft</span><span class="sxs-lookup"><span data-stu-id="0eefa-124">originLeft</span></span>

<span data-ttu-id="0eefa-125">O local de origem do elemento para receber o foco.</span><span class="sxs-lookup"><span data-stu-id="0eefa-125">The origin left location of the element to be given focus.</span></span>

<span data-ttu-id="0eefa-126">Essa propriedade é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="0eefa-126">This property is read-only.</span></span>

```js
var originLeft = FocusNavigationEvent.originLeft;
```

#### <span data-ttu-id="0eefa-127">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="0eefa-127">Property value</span></span>
<span data-ttu-id="0eefa-128">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="0eefa-128">Type: **float**</span></span>

### <span data-ttu-id="0eefa-129">originTop</span><span class="sxs-lookup"><span data-stu-id="0eefa-129">originTop</span></span>

<span data-ttu-id="0eefa-130">O local de origem superior do elemento a receber o foco.</span><span class="sxs-lookup"><span data-stu-id="0eefa-130">The origin top location of the element to be given focus.</span></span>

<span data-ttu-id="0eefa-131">Essa propriedade é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="0eefa-131">This property is read-only.</span></span>

```js
var originTop = FocusNavigationEvent.originTop;
```

#### <span data-ttu-id="0eefa-132">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="0eefa-132">Property value</span></span>
<span data-ttu-id="0eefa-133">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="0eefa-133">Type: **float**</span></span>

### <span data-ttu-id="0eefa-134">originWidth</span><span class="sxs-lookup"><span data-stu-id="0eefa-134">originWidth</span></span>

<span data-ttu-id="0eefa-135">O local da largura de origem do elemento a receber o foco.</span><span class="sxs-lookup"><span data-stu-id="0eefa-135">The origin width location of the element to be given focus.</span></span>

<span data-ttu-id="0eefa-136">Essa propriedade é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="0eefa-136">This property is read-only.</span></span>

```js
var originWidth = FocusNavigationEvent.originWidth;
```

#### <span data-ttu-id="0eefa-137">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="0eefa-137">Property value</span></span>
<span data-ttu-id="0eefa-138">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="0eefa-138">Type: **float**</span></span>

