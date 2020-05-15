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
ms.openlocfilehash: 748c4affa73001270e2cf97b3d19db8c8ed23686
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652737"
---
# <span data-ttu-id="76866-104">interface IWebView2ProcessFailedEventArgs</span><span class="sxs-lookup"><span data-stu-id="76866-104">interface IWebView2ProcessFailedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="76866-105">Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="76866-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="76866-106">Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.</span><span class="sxs-lookup"><span data-stu-id="76866-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2ProcessFailedEventArgs
  : public IUnknown
```

<span data-ttu-id="76866-107">Args de evento para o evento ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="76866-107">Event args for the ProcessFailed event.</span></span>

## <span data-ttu-id="76866-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="76866-108">Summary</span></span>

 <span data-ttu-id="76866-109">Parte</span><span class="sxs-lookup"><span data-stu-id="76866-109">Members</span></span>                        | <span data-ttu-id="76866-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="76866-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="76866-111">get_ProcessFailedKind</span><span class="sxs-lookup"><span data-stu-id="76866-111">get_ProcessFailedKind</span></span>](#get_processfailedkind) | <span data-ttu-id="76866-112">O tipo de falha de processo ocorrida.</span><span class="sxs-lookup"><span data-stu-id="76866-112">The kind of process failure that has occurred.</span></span>

## <span data-ttu-id="76866-113">Parte</span><span class="sxs-lookup"><span data-stu-id="76866-113">Members</span></span>

#### <span data-ttu-id="76866-114">get_ProcessFailedKind</span><span class="sxs-lookup"><span data-stu-id="76866-114">get_ProcessFailedKind</span></span> 

<span data-ttu-id="76866-115">O tipo de falha de processo ocorrida.</span><span class="sxs-lookup"><span data-stu-id="76866-115">The kind of process failure that has occurred.</span></span>

> <span data-ttu-id="76866-116">público HRESULT [get_ProcessFailedKind](#get_processfailedkind)(WEBVIEW2_PROCESS_FAILED_KIND \* ProcessFailedKind)</span><span class="sxs-lookup"><span data-stu-id="76866-116">public HRESULT [get_ProcessFailedKind](#get_processfailedkind)(WEBVIEW2_PROCESS_FAILED_KIND \* processFailedKind)</span></span>

