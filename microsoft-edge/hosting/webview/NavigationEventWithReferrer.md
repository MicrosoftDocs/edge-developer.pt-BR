---
description: Contém informações de referenciais sobre a navegação
title: Objeto NavigationEventWithReferrer
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/10/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, aplicativos do Windows 10, UWP, Edge
ms.openlocfilehash: 72c8a213f632e9e74145de9c34b949adf074cd22
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752113"
---
# <span data-ttu-id="8f235-104">Objeto NavigationEventWithReferrer</span><span class="sxs-lookup"><span data-stu-id="8f235-104">NavigationEventWithReferrer object</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="8f235-105">Um objeto que representa um evento acionado quando a navegação é iniciada e a navegação contém um referenciador.</span><span class="sxs-lookup"><span data-stu-id="8f235-105">An object that represents an event fired when navigation is initiated and the navigation contains a referer.</span></span>  

## <span data-ttu-id="8f235-106">Propriedades</span><span class="sxs-lookup"><span data-stu-id="8f235-106">Properties</span></span>  

### <span data-ttu-id="8f235-107">referência</span><span class="sxs-lookup"><span data-stu-id="8f235-107">referer</span></span>

<span data-ttu-id="8f235-108">O URI (Uniform Resource Identifier) da página no [WebView](../webview.md) que solicita navegação.</span><span class="sxs-lookup"><span data-stu-id="8f235-108">The Uniform Resource Identifier (URI) of the page in the [webview](../webview.md) requesting navigation.</span></span>  

<span data-ttu-id="8f235-109">Essa propriedade é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="8f235-109">This property is read-only.</span></span>  

#### <span data-ttu-id="8f235-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="8f235-110">Property value</span></span>  

<span data-ttu-id="8f235-111">Tipo: **DOMString**</span><span class="sxs-lookup"><span data-stu-id="8f235-111">Type: **DOMString**</span></span>  

```javascript
var referer = NavigationEventWithReferrer.referer;
```  

### <span data-ttu-id="8f235-112">uri</span><span class="sxs-lookup"><span data-stu-id="8f235-112">uri</span></span>  

<span data-ttu-id="8f235-113">O URI (Uniform Resource Identifier) do destino da navegação.</span><span class="sxs-lookup"><span data-stu-id="8f235-113">The Uniform Resource Identifier (URI) of the destination of the navigation.</span></span>  

<span data-ttu-id="8f235-114">Essa propriedade é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="8f235-114">This property is read-only.</span></span>  

```javascript
var uri = NavigationEventWithReferrer.uri;
```  

#### <span data-ttu-id="8f235-115">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="8f235-115">Property value</span></span>  

<span data-ttu-id="8f235-116">Tipo: **DOMString**</span><span class="sxs-lookup"><span data-stu-id="8f235-116">Type: **DOMString**</span></span>  
