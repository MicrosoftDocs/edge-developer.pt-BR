---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.8.355-WebView2 Win32 C++ IWebView2ProcessFailedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge
ms.openlocfilehash: 5ceb24d0d20f580e14e0d5af7ec09881c9ab0eb2
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878243"
---
# <span data-ttu-id="be1a3-104">0.8.355-IWebView2ProcessFailedEventArgs de interface</span><span class="sxs-lookup"><span data-stu-id="be1a3-104">0.8.355 - interface IWebView2ProcessFailedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="be1a3-105">Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="be1a3-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="be1a3-106">Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.</span><span class="sxs-lookup"><span data-stu-id="be1a3-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2ProcessFailedEventArgs
  : public IUnknown
```

<span data-ttu-id="be1a3-107">Args de evento para o evento ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="be1a3-107">Event args for the ProcessFailed event.</span></span>

## <span data-ttu-id="be1a3-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="be1a3-108">Summary</span></span>

 <span data-ttu-id="be1a3-109">Parte</span><span class="sxs-lookup"><span data-stu-id="be1a3-109">Members</span></span>                        | <span data-ttu-id="be1a3-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="be1a3-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="be1a3-111">get_ProcessFailedKind</span><span class="sxs-lookup"><span data-stu-id="be1a3-111">get_ProcessFailedKind</span></span>](#get_processfailedkind) | <span data-ttu-id="be1a3-112">O tipo de falha de processo ocorrida.</span><span class="sxs-lookup"><span data-stu-id="be1a3-112">The kind of process failure that has occurred.</span></span>

## <span data-ttu-id="be1a3-113">Parte</span><span class="sxs-lookup"><span data-stu-id="be1a3-113">Members</span></span>

#### <span data-ttu-id="be1a3-114">get_ProcessFailedKind</span><span class="sxs-lookup"><span data-stu-id="be1a3-114">get_ProcessFailedKind</span></span> 

<span data-ttu-id="be1a3-115">O tipo de falha de processo ocorrida.</span><span class="sxs-lookup"><span data-stu-id="be1a3-115">The kind of process failure that has occurred.</span></span>

> <span data-ttu-id="be1a3-116">público HRESULT [get_ProcessFailedKind](#get_processfailedkind)(WEBVIEW2_PROCESS_FAILED_KIND \* ProcessFailedKind)</span><span class="sxs-lookup"><span data-stu-id="be1a3-116">public HRESULT [get_ProcessFailedKind](#get_processfailedkind)(WEBVIEW2_PROCESS_FAILED_KIND \* processFailedKind)</span></span>

