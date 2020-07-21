---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2ProcessFailedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: a19f8c445d7ff1f6bee24cdd8871c28d41eedebe
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886406"
---
# <span data-ttu-id="35fe9-104">0.9.430-ICoreWebView2ProcessFailedEventArgs de interface</span><span class="sxs-lookup"><span data-stu-id="35fe9-104">0.9.430 - interface ICoreWebView2ProcessFailedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2ProcessFailedEventArgs
  : public IUnknown
```

<span data-ttu-id="35fe9-105">Args de evento para o evento ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="35fe9-105">Event args for the ProcessFailed event.</span></span>

## <span data-ttu-id="35fe9-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="35fe9-106">Summary</span></span>

 <span data-ttu-id="35fe9-107">Parte</span><span class="sxs-lookup"><span data-stu-id="35fe9-107">Members</span></span>                        | <span data-ttu-id="35fe9-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="35fe9-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="35fe9-109">get_ProcessFailedKind</span><span class="sxs-lookup"><span data-stu-id="35fe9-109">get_ProcessFailedKind</span></span>](#get_processfailedkind) | <span data-ttu-id="35fe9-110">O tipo de falha de processo ocorrida.</span><span class="sxs-lookup"><span data-stu-id="35fe9-110">The kind of process failure that has occurred.</span></span>

## <span data-ttu-id="35fe9-111">Parte</span><span class="sxs-lookup"><span data-stu-id="35fe9-111">Members</span></span>

#### <span data-ttu-id="35fe9-112">get_ProcessFailedKind</span><span class="sxs-lookup"><span data-stu-id="35fe9-112">get_ProcessFailedKind</span></span> 

<span data-ttu-id="35fe9-113">O tipo de falha de processo ocorrida.</span><span class="sxs-lookup"><span data-stu-id="35fe9-113">The kind of process failure that has occurred.</span></span>

> <span data-ttu-id="35fe9-114">público HRESULT [get_ProcessFailedKind](#get_processfailedkind)(CORE_WEBVIEW2_PROCESS_FAILED_KIND \* ProcessFailedKind)</span><span class="sxs-lookup"><span data-stu-id="35fe9-114">public HRESULT [get_ProcessFailedKind](#get_processfailedkind)(CORE_WEBVIEW2_PROCESS_FAILED_KIND \* processFailedKind)</span></span>

