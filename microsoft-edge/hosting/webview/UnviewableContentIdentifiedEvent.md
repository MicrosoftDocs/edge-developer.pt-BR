---
description: Indica que o WebView está tentando baixar um arquivo sem suporte.
title: Objeto UnviewableContentIdentifiedEvent
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/10/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, aplicativos do Windows 10, UWP, Edge
ms.openlocfilehash: 0179522f3eaf0813531084eb996ee9d392e8249d
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752010"
---
# <span data-ttu-id="3b0b9-104">Objeto UnviewableContentIdentifiedEvent</span><span class="sxs-lookup"><span data-stu-id="3b0b9-104">UnviewableContentIdentifiedEvent object</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="3b0b9-105">Indica que o [WebView](../webview.md) está tentando navegar para um arquivo de um tipo de conteúdo sem suporte.</span><span class="sxs-lookup"><span data-stu-id="3b0b9-105">Indicates the [webview](../webview.md) is attempting to navigate to a file of an unsupported content type.</span></span>  

## <span data-ttu-id="3b0b9-106">Propriedades</span><span class="sxs-lookup"><span data-stu-id="3b0b9-106">Properties</span></span>  

### <span data-ttu-id="3b0b9-107">mediaType</span><span class="sxs-lookup"><span data-stu-id="3b0b9-107">mediaType</span></span>  

<span data-ttu-id="3b0b9-108">Obtém o tipo de conteúdo do conteúdo inviewável.</span><span class="sxs-lookup"><span data-stu-id="3b0b9-108">Gets the content type of the unviewable content.</span></span>  

<span data-ttu-id="3b0b9-109">Essa propriedade é somente leitura</span><span class="sxs-lookup"><span data-stu-id="3b0b9-109">This property is read-only</span></span>  

```javascript
var mediaType = UnviewableContentIdentifiedEvent.mediaType;
```  

#### <span data-ttu-id="3b0b9-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="3b0b9-110">Property value</span></span>  

<span data-ttu-id="3b0b9-111">Tipo: **DOMString**</span><span class="sxs-lookup"><span data-stu-id="3b0b9-111">Type: **DOMString**</span></span>  

### <span data-ttu-id="3b0b9-112">referência</span><span class="sxs-lookup"><span data-stu-id="3b0b9-112">referer</span></span>  

<span data-ttu-id="3b0b9-113">O URI (Uniform Resource Identifier) da página no [WebView](../webview.md) que solicita navegação.</span><span class="sxs-lookup"><span data-stu-id="3b0b9-113">The Uniform Resource Identifier (URI) of the page in the [webview](../webview.md) requesting navigation.</span></span>  

<span data-ttu-id="3b0b9-114">Essa propriedade é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="3b0b9-114">This property is read-only.</span></span>  

```javascript
var referer = NavigationEventWithReferrer.referer;
```  

#### <span data-ttu-id="3b0b9-115">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="3b0b9-115">Property value</span></span>  

<span data-ttu-id="3b0b9-116">Tipo: **DOMString**</span><span class="sxs-lookup"><span data-stu-id="3b0b9-116">Type: **DOMString**</span></span>  

### <span data-ttu-id="3b0b9-117">uri</span><span class="sxs-lookup"><span data-stu-id="3b0b9-117">uri</span></span>  

<span data-ttu-id="3b0b9-118">O URI (Uniform Resource Identifier) do destino da navegação.</span><span class="sxs-lookup"><span data-stu-id="3b0b9-118">The Uniform Resource Identifier (URI) of the destination of the navigation.</span></span>  

<span data-ttu-id="3b0b9-119">Essa propriedade é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="3b0b9-119">This property is read-only.</span></span>  

```javascript
var uri = NavigationEventWithReferrer.uri;
```  

#### <span data-ttu-id="3b0b9-120">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="3b0b9-120">Property value</span></span>  

<span data-ttu-id="3b0b9-121">Tipo: **DOMString**</span><span class="sxs-lookup"><span data-stu-id="3b0b9-121">Type: **DOMString**</span></span>  
