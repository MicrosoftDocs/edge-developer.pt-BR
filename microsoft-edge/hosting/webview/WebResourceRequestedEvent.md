---
description: Um evento que é acionado quando uma solicitação HTTP é feita.
title: Objeto WebResourceRequestedEvent
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/10/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, aplicativos do Windows 10, UWP, Edge
ms.openlocfilehash: 3d2bb54cc5d60aec5391f0e3fdd427c8ba8a3dab
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/18/2020
ms.locfileid: "10751979"
---
# <span data-ttu-id="90abb-104">Objeto WebResourceRequestedEvent</span><span class="sxs-lookup"><span data-stu-id="90abb-104">WebResourceRequestedEvent object</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="90abb-105">Um evento que é acionado quando uma solicitação HTTP é feita.</span><span class="sxs-lookup"><span data-stu-id="90abb-105">An event that is fired when an HTTP request is made.</span></span>  

## <span data-ttu-id="90abb-106">Propriedades</span><span class="sxs-lookup"><span data-stu-id="90abb-106">Properties</span></span>  

### <span data-ttu-id="90abb-107">args</span><span class="sxs-lookup"><span data-stu-id="90abb-107">args</span></span>  

<span data-ttu-id="90abb-108">Informações sobre a solicitação do recurso.</span><span class="sxs-lookup"><span data-stu-id="90abb-108">Information about the resource request.</span></span>  <span data-ttu-id="90abb-109">Isso é um [Windows. Web. UI. WebViewControlWebResourceRequestedEventArgs](/uwp/api/windows.web.ui.webviewcontrolwebresourcerequestedeventargs).</span><span class="sxs-lookup"><span data-stu-id="90abb-109">This is a [Windows.Web.UI.WebViewControlWebResourceRequestedEventArgs](/uwp/api/windows.web.ui.webviewcontrolwebresourcerequestedeventargs).</span></span>  

<span data-ttu-id="90abb-110">Essa propriedade é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="90abb-110">This property is read-only.</span></span>  

```javascript
var args = webResourceRequestedEventArgs.args;
var request = args.request;
```  

#### <span data-ttu-id="90abb-111">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="90abb-111">Property value</span></span>  

<span data-ttu-id="90abb-112">Tipo: **qualquer**</span><span class="sxs-lookup"><span data-stu-id="90abb-112">Type: **any**</span></span>  
