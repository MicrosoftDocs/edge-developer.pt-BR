---
description: Indica que o WebView está tentando baixar um arquivo sem suporte.
title: Objeto UnviewableContentIdentifiedEvent
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/25/2018
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, aplicativos do Windows 10, UWP, Edge
ms.openlocfilehash: cec85ca2d5458a05cfd88210907523f25fb4af95
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10560491"
---
# <span data-ttu-id="70dfc-104">Objeto UnviewableContentIdentifiedEvent</span><span class="sxs-lookup"><span data-stu-id="70dfc-104">UnviewableContentIdentifiedEvent object</span></span>

<span data-ttu-id="70dfc-105">Indica que o [WebView](../webview.md) está tentando navegar para um arquivo de um tipo de conteúdo sem suporte.</span><span class="sxs-lookup"><span data-stu-id="70dfc-105">Indicates the [webview](../webview.md) is attempting to navigate to a file of an unsupported content type.</span></span> 

## <span data-ttu-id="70dfc-106">Propriedades</span><span class="sxs-lookup"><span data-stu-id="70dfc-106">Properties</span></span>

### <span data-ttu-id="70dfc-107">mediaType</span><span class="sxs-lookup"><span data-stu-id="70dfc-107">mediaType</span></span>

<span data-ttu-id="70dfc-108">Obtém o tipo de conteúdo do conteúdo inviewável.</span><span class="sxs-lookup"><span data-stu-id="70dfc-108">Gets the content type of the unviewable content.</span></span>

<span data-ttu-id="70dfc-109">Essa propriedade é somente leitura</span><span class="sxs-lookup"><span data-stu-id="70dfc-109">This property is read-only</span></span>

```js
var mediaType = UnviewableContentIdentifiedEvent.mediaType;
```

#### <span data-ttu-id="70dfc-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="70dfc-110">Property value</span></span>
<span data-ttu-id="70dfc-111">Tipo: **DOMString**</span><span class="sxs-lookup"><span data-stu-id="70dfc-111">Type: **DOMString**</span></span>

### <span data-ttu-id="70dfc-112">referência</span><span class="sxs-lookup"><span data-stu-id="70dfc-112">referer</span></span>

<span data-ttu-id="70dfc-113">O URI (Uniform Resource Identifier) da página no [WebView](../webview.md) que solicita navegação.</span><span class="sxs-lookup"><span data-stu-id="70dfc-113">The Uniform Resource Identifier (URI) of the page in the [webview](../webview.md) requesting navigation.</span></span>

<span data-ttu-id="70dfc-114">Essa propriedade é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="70dfc-114">This property is read-only.</span></span>


```js
var referer = NavigationEventWithReferrer.referer;
```

#### <span data-ttu-id="70dfc-115">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="70dfc-115">Property value</span></span>
<span data-ttu-id="70dfc-116">Tipo: **DOMString**</span><span class="sxs-lookup"><span data-stu-id="70dfc-116">Type: **DOMString**</span></span>

### <span data-ttu-id="70dfc-117">uri</span><span class="sxs-lookup"><span data-stu-id="70dfc-117">uri</span></span>

<span data-ttu-id="70dfc-118">O URI (Uniform Resource Identifier) do destino da navegação.</span><span class="sxs-lookup"><span data-stu-id="70dfc-118">The Uniform Resource Identifier (URI) of the destination of the navigation.</span></span>

<span data-ttu-id="70dfc-119">Essa propriedade é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="70dfc-119">This property is read-only.</span></span>

```js
var uri = NavigationEventWithReferrer.uri;
```

#### <span data-ttu-id="70dfc-120">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="70dfc-120">Property value</span></span>
<span data-ttu-id="70dfc-121">Tipo: **DOMString**</span><span class="sxs-lookup"><span data-stu-id="70dfc-121">Type: **DOMString**</span></span>
