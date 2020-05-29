---
description: Contém informações de referenciais sobre a navegação
title: Objeto NavigationEventWithReferrer
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/22/2018
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, aplicativos do Windows 10, UWP, Edge
ms.openlocfilehash: b11f60724387d996d0a730965602b5ead6a84145
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10560959"
---
# <span data-ttu-id="aa3af-104">Objeto NavigationEventWithReferrer</span><span class="sxs-lookup"><span data-stu-id="aa3af-104">NavigationEventWithReferrer object</span></span>

<span data-ttu-id="aa3af-105">Um objeto que representa um evento acionado quando a navegação é iniciada e a navegação contém um referenciador.</span><span class="sxs-lookup"><span data-stu-id="aa3af-105">An object that represents an event fired when navigation is initiated and the navigation contains a referer.</span></span>

## <span data-ttu-id="aa3af-106">Propriedades</span><span class="sxs-lookup"><span data-stu-id="aa3af-106">Properties</span></span>

### <span data-ttu-id="aa3af-107">referência</span><span class="sxs-lookup"><span data-stu-id="aa3af-107">referer</span></span>

<span data-ttu-id="aa3af-108">O URI (Uniform Resource Identifier) da página no [WebView](../webview.md) que solicita navegação.</span><span class="sxs-lookup"><span data-stu-id="aa3af-108">The Uniform Resource Identifier (URI) of the page in the [webview](../webview.md) requesting navigation.</span></span>

<span data-ttu-id="aa3af-109">Essa propriedade é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="aa3af-109">This property is read-only.</span></span>

#### <span data-ttu-id="aa3af-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="aa3af-110">Property value</span></span>
<span data-ttu-id="aa3af-111">Tipo: **DOMString**</span><span class="sxs-lookup"><span data-stu-id="aa3af-111">Type: **DOMString**</span></span>


```js
var referer = NavigationEventWithReferrer.referer;
```

### <span data-ttu-id="aa3af-112">uri</span><span class="sxs-lookup"><span data-stu-id="aa3af-112">uri</span></span>

<span data-ttu-id="aa3af-113">O URI (Uniform Resource Identifier) do destino da navegação.</span><span class="sxs-lookup"><span data-stu-id="aa3af-113">The Uniform Resource Identifier (URI) of the destination of the navigation.</span></span>

<span data-ttu-id="aa3af-114">Essa propriedade é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="aa3af-114">This property is read-only.</span></span>

```js
var uri = NavigationEventWithReferrer.uri;
```

#### <span data-ttu-id="aa3af-115">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="aa3af-115">Property value</span></span>
<span data-ttu-id="aa3af-116">Tipo: **DOMString**</span><span class="sxs-lookup"><span data-stu-id="aa3af-116">Type: **DOMString**</span></span>
