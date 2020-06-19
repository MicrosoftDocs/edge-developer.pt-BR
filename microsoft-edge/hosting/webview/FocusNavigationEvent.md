---
description: O objeto despachado de um evento Focus que contém o motivo e a localização da navegação
title: Objeto FocusNavigationEvent
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/10/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, aplicativos do Windows 10, UWP, Edge
ms.openlocfilehash: 88f0a4ef8834c6e851f81ee10bf4202a0429f969
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752161"
---
# <span data-ttu-id="42b2a-104">Objeto FocusNavigationEvent</span><span class="sxs-lookup"><span data-stu-id="42b2a-104">FocusNavigationEvent object</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="42b2a-105">O objeto despachado da [**NavigateFocus**](../webview.md#navigatefocus) / [**DepartingFocus**](../webview.md#departingfocus) que contém o [**NavigationReason**](#navigationreason) e o local.</span><span class="sxs-lookup"><span data-stu-id="42b2a-105">The dispatched object from [**NavigateFocus**](../webview.md#navigatefocus)/[**DepartingFocus**](../webview.md#departingfocus) containing the [**NavigationReason**](#navigationreason) and location.</span></span>  

## <span data-ttu-id="42b2a-106">Métodos</span><span class="sxs-lookup"><span data-stu-id="42b2a-106">Methods</span></span>  

### <span data-ttu-id="42b2a-107">requestFocus</span><span class="sxs-lookup"><span data-stu-id="42b2a-107">requestFocus</span></span>  

<span data-ttu-id="42b2a-108">Chamado para mover o foco do aplicativo para o WebView.</span><span class="sxs-lookup"><span data-stu-id="42b2a-108">Called to move focus from the app to the webview.</span></span>  

### <span data-ttu-id="42b2a-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="42b2a-109">Parameters</span></span>  

<span data-ttu-id="42b2a-110">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="42b2a-110">This method does not have parameters.</span></span>  

### <span data-ttu-id="42b2a-111">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="42b2a-111">Return value</span></span>  

<span data-ttu-id="42b2a-112">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="42b2a-112">This method does not return a value.</span></span>  

## <span data-ttu-id="42b2a-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="42b2a-113">Properties</span></span>  

### <span data-ttu-id="42b2a-114">navigationReason</span><span class="sxs-lookup"><span data-stu-id="42b2a-114">navigationReason</span></span>  

<span data-ttu-id="42b2a-115">O tipo enumerado **NavigationReason**, "Left", "up", "Right" ou "Down".</span><span class="sxs-lookup"><span data-stu-id="42b2a-115">Enumerated type **NavigationReason**, either "left", "up", "right", or "down".</span></span>  

<span data-ttu-id="42b2a-116">Essa propriedade é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="42b2a-116">This property is read-only.</span></span>  

```javascript
var navigationReason = FocusNavigationEvent.navigationReason;
```  

#### <span data-ttu-id="42b2a-117">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="42b2a-117">Property value</span></span>  

<span data-ttu-id="42b2a-118">Tipo: **NavigationReason**</span><span class="sxs-lookup"><span data-stu-id="42b2a-118">Type: **NavigationReason**</span></span>  

### <span data-ttu-id="42b2a-119">originHeight</span><span class="sxs-lookup"><span data-stu-id="42b2a-119">originHeight</span></span>  

<span data-ttu-id="42b2a-120">O local da altura da origem do elemento a receber o foco.</span><span class="sxs-lookup"><span data-stu-id="42b2a-120">The origin height location of the element to be given focus.</span></span>  

<span data-ttu-id="42b2a-121">Essa propriedade é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="42b2a-121">This property is read-only.</span></span>  

```javascript
var originWoriginHeightidth = FocusNavigationEvent.originHeight;
```  

#### <span data-ttu-id="42b2a-122">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="42b2a-122">Property value</span></span>  

<span data-ttu-id="42b2a-123">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="42b2a-123">Type: **float**</span></span>  

### <span data-ttu-id="42b2a-124">originLeft</span><span class="sxs-lookup"><span data-stu-id="42b2a-124">originLeft</span></span>  

<span data-ttu-id="42b2a-125">O local de origem do elemento para receber o foco.</span><span class="sxs-lookup"><span data-stu-id="42b2a-125">The origin left location of the element to be given focus.</span></span>  

<span data-ttu-id="42b2a-126">Essa propriedade é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="42b2a-126">This property is read-only.</span></span>  

```javascript
var originLeft = FocusNavigationEvent.originLeft;
```  

#### <span data-ttu-id="42b2a-127">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="42b2a-127">Property value</span></span>  

<span data-ttu-id="42b2a-128">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="42b2a-128">Type: **float**</span></span>  

### <span data-ttu-id="42b2a-129">originTop</span><span class="sxs-lookup"><span data-stu-id="42b2a-129">originTop</span></span>  

<span data-ttu-id="42b2a-130">O local de origem superior do elemento a receber o foco.</span><span class="sxs-lookup"><span data-stu-id="42b2a-130">The origin top location of the element to be given focus.</span></span>  

<span data-ttu-id="42b2a-131">Essa propriedade é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="42b2a-131">This property is read-only.</span></span>  

```javascript
var originTop = FocusNavigationEvent.originTop;
```  

#### <span data-ttu-id="42b2a-132">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="42b2a-132">Property value</span></span>  

<span data-ttu-id="42b2a-133">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="42b2a-133">Type: **float**</span></span>  

### <span data-ttu-id="42b2a-134">originWidth</span><span class="sxs-lookup"><span data-stu-id="42b2a-134">originWidth</span></span>  

<span data-ttu-id="42b2a-135">O local da largura de origem do elemento a receber o foco.</span><span class="sxs-lookup"><span data-stu-id="42b2a-135">The origin width location of the element to be given focus.</span></span>  

<span data-ttu-id="42b2a-136">Essa propriedade é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="42b2a-136">This property is read-only.</span></span>  

```javascript
var originWidth = FocusNavigationEvent.originWidth;
```  

#### <span data-ttu-id="42b2a-137">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="42b2a-137">Property value</span></span>  

<span data-ttu-id="42b2a-138">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="42b2a-138">Type: **float**</span></span>  
