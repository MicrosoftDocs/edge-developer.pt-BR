---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: Microsoft Edge WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/09/2019
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge
ms.openlocfilehash: c23e6bcd18e3b0fe7d2ee9b279e65fc81fe89d3d
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652406"
---
# <span data-ttu-id="0c0fc-104">interface IWebView2WebResourceRequestedEventArgs2</span><span class="sxs-lookup"><span data-stu-id="0c0fc-104">interface IWebView2WebResourceRequestedEventArgs2</span></span> 

> [!NOTE]
> <span data-ttu-id="0c0fc-105">Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="0c0fc-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="0c0fc-106">Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.</span><span class="sxs-lookup"><span data-stu-id="0c0fc-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2WebResourceRequestedEventArgs2
  : public IWebView2WebResourceRequestedEventArgs
```

<span data-ttu-id="0c0fc-107">Args de evento para o evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="0c0fc-107">Event args for the WebResourceRequested event.</span></span>

## <span data-ttu-id="0c0fc-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="0c0fc-108">Summary</span></span>

 <span data-ttu-id="0c0fc-109">Parte</span><span class="sxs-lookup"><span data-stu-id="0c0fc-109">Members</span></span>                        | <span data-ttu-id="0c0fc-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="0c0fc-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="0c0fc-111">get_ResourceContext</span><span class="sxs-lookup"><span data-stu-id="0c0fc-111">get_ResourceContext</span></span>](#get_resourcecontext) | <span data-ttu-id="0c0fc-112">Os contextos de solicitação de recurso da Web.</span><span class="sxs-lookup"><span data-stu-id="0c0fc-112">The web resource request contexts.</span></span>

## <span data-ttu-id="0c0fc-113">Parte</span><span class="sxs-lookup"><span data-stu-id="0c0fc-113">Members</span></span>

#### <span data-ttu-id="0c0fc-114">get_ResourceContext</span><span class="sxs-lookup"><span data-stu-id="0c0fc-114">get_ResourceContext</span></span> 

<span data-ttu-id="0c0fc-115">Os contextos de solicitação de recurso da Web.</span><span class="sxs-lookup"><span data-stu-id="0c0fc-115">The web resource request contexts.</span></span>

> <span data-ttu-id="0c0fc-116">[get_ResourceContext](#get_resourcecontext)público HRESULT (WEBVIEW2_WEB_RESOURCE_CONTEXT \* contexto)</span><span class="sxs-lookup"><span data-stu-id="0c0fc-116">public HRESULT [get_ResourceContext](#get_resourcecontext)(WEBVIEW2_WEB_RESOURCE_CONTEXT \* context)</span></span>

