---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.8.355-WebView2 Win32 C++ IWebView2WebResourceRequestedEventArgs2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge
ms.openlocfilehash: 7f710b4da71a4a4e61869f06e5d2a4a95a2d0891
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885706"
---
# <span data-ttu-id="788d3-104">0.8.355-IWebView2WebResourceRequestedEventArgs2 de interface</span><span class="sxs-lookup"><span data-stu-id="788d3-104">0.8.355 - interface IWebView2WebResourceRequestedEventArgs2</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2WebResourceRequestedEventArgs2
  : public IWebView2WebResourceRequestedEventArgs
```

<span data-ttu-id="788d3-105">Args de evento para o evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="788d3-105">Event args for the WebResourceRequested event.</span></span>

## <span data-ttu-id="788d3-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="788d3-106">Summary</span></span>

 <span data-ttu-id="788d3-107">Parte</span><span class="sxs-lookup"><span data-stu-id="788d3-107">Members</span></span>                        | <span data-ttu-id="788d3-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="788d3-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="788d3-109">get_ResourceContext</span><span class="sxs-lookup"><span data-stu-id="788d3-109">get_ResourceContext</span></span>](#get_resourcecontext) | <span data-ttu-id="788d3-110">Os contextos de solicitação de recurso da Web.</span><span class="sxs-lookup"><span data-stu-id="788d3-110">The web resource request contexts.</span></span>

## <span data-ttu-id="788d3-111">Parte</span><span class="sxs-lookup"><span data-stu-id="788d3-111">Members</span></span>

#### <span data-ttu-id="788d3-112">get_ResourceContext</span><span class="sxs-lookup"><span data-stu-id="788d3-112">get_ResourceContext</span></span> 

<span data-ttu-id="788d3-113">Os contextos de solicitação de recurso da Web.</span><span class="sxs-lookup"><span data-stu-id="788d3-113">The web resource request contexts.</span></span>

> <span data-ttu-id="788d3-114">[get_ResourceContext](#get_resourcecontext)público HRESULT (WEBVIEW2_WEB_RESOURCE_CONTEXT \* contexto)</span><span class="sxs-lookup"><span data-stu-id="788d3-114">public HRESULT [get_ResourceContext](#get_resourcecontext)(WEBVIEW2_WEB_RESOURCE_CONTEXT \* context)</span></span>

