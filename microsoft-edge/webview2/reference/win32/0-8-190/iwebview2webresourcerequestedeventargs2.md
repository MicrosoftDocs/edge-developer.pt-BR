---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.8.355-WebView2 Win32 C++ IWebView2WebResourceRequestedEventArgs2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge
ms.openlocfilehash: 80ea596f28d1afeb451ce20d495961ca4eed507a
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878110"
---
# <span data-ttu-id="ac2db-104">0.8.355-IWebView2WebResourceRequestedEventArgs2 de interface</span><span class="sxs-lookup"><span data-stu-id="ac2db-104">0.8.355 - interface IWebView2WebResourceRequestedEventArgs2</span></span> 

> [!NOTE]
> <span data-ttu-id="ac2db-105">Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="ac2db-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="ac2db-106">Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.</span><span class="sxs-lookup"><span data-stu-id="ac2db-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2WebResourceRequestedEventArgs2
  : public IWebView2WebResourceRequestedEventArgs
```

<span data-ttu-id="ac2db-107">Args de evento para o evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="ac2db-107">Event args for the WebResourceRequested event.</span></span>

## <span data-ttu-id="ac2db-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="ac2db-108">Summary</span></span>

 <span data-ttu-id="ac2db-109">Parte</span><span class="sxs-lookup"><span data-stu-id="ac2db-109">Members</span></span>                        | <span data-ttu-id="ac2db-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="ac2db-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="ac2db-111">get_ResourceContext</span><span class="sxs-lookup"><span data-stu-id="ac2db-111">get_ResourceContext</span></span>](#get_resourcecontext) | <span data-ttu-id="ac2db-112">Os contextos de solicitação de recurso da Web.</span><span class="sxs-lookup"><span data-stu-id="ac2db-112">The web resource request contexts.</span></span>

## <span data-ttu-id="ac2db-113">Parte</span><span class="sxs-lookup"><span data-stu-id="ac2db-113">Members</span></span>

#### <span data-ttu-id="ac2db-114">get_ResourceContext</span><span class="sxs-lookup"><span data-stu-id="ac2db-114">get_ResourceContext</span></span> 

<span data-ttu-id="ac2db-115">Os contextos de solicitação de recurso da Web.</span><span class="sxs-lookup"><span data-stu-id="ac2db-115">The web resource request contexts.</span></span>

> <span data-ttu-id="ac2db-116">[get_ResourceContext](#get_resourcecontext)público HRESULT (WEBVIEW2_WEB_RESOURCE_CONTEXT \* contexto)</span><span class="sxs-lookup"><span data-stu-id="ac2db-116">public HRESULT [get_ResourceContext](#get_resourcecontext)(WEBVIEW2_WEB_RESOURCE_CONTEXT \* context)</span></span>

