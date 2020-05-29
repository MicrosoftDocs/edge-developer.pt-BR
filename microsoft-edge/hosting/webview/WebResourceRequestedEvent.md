---
description: Um evento que é acionado quando uma solicitação HTTP é feita.
title: Objeto WebResourceRequestedEvent
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/15/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, aplicativos do Windows 10, UWP, Edge
ms.openlocfilehash: 79cff0d8fd68e3b5747008f343b5b46fb8093013
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10560488"
---
# <span data-ttu-id="ea89b-104">Objeto WebResourceRequestedEvent</span><span class="sxs-lookup"><span data-stu-id="ea89b-104">WebResourceRequestedEvent object</span></span>

<span data-ttu-id="ea89b-105">Um evento que é acionado quando uma solicitação HTTP é feita.</span><span class="sxs-lookup"><span data-stu-id="ea89b-105">An event that is fired when an HTTP request is made.</span></span>

## <span data-ttu-id="ea89b-106">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ea89b-106">Properties</span></span>

### <span data-ttu-id="ea89b-107">args</span><span class="sxs-lookup"><span data-stu-id="ea89b-107">args</span></span>

<span data-ttu-id="ea89b-108">Informações sobre a solicitação do recurso.</span><span class="sxs-lookup"><span data-stu-id="ea89b-108">Information about the resource request.</span></span> <span data-ttu-id="ea89b-109">Isso é um [Windows. Web. UI. WebViewControlWebResourceRequestedEventArgs](/uwp/api/windows.web.ui.webviewcontrolwebresourcerequestedeventargs).</span><span class="sxs-lookup"><span data-stu-id="ea89b-109">This is a [Windows.Web.UI.WebViewControlWebResourceRequestedEventArgs](/uwp/api/windows.web.ui.webviewcontrolwebresourcerequestedeventargs).</span></span>

<span data-ttu-id="ea89b-110">Essa propriedade é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="ea89b-110">This property is read-only.</span></span>

```js
var args = webResourceRequestedEventArgs.args;
var request = args.request;
```

#### <span data-ttu-id="ea89b-111">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="ea89b-111">Property value</span></span>
<span data-ttu-id="ea89b-112">Tipo: **qualquer**</span><span class="sxs-lookup"><span data-stu-id="ea89b-112">Type: **any**</span></span>

