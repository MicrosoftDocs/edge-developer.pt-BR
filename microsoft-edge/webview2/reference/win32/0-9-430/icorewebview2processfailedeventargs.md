---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: Microsoft Edge WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/24/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: 8fba2759ce0e264dcde515ee1191ec819f26eef9
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652568"
---
# <span data-ttu-id="30f5d-104">interface ICoreWebView2ProcessFailedEventArgs</span><span class="sxs-lookup"><span data-stu-id="30f5d-104">interface ICoreWebView2ProcessFailedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="30f5d-105">Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="30f5d-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="30f5d-106">Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.</span><span class="sxs-lookup"><span data-stu-id="30f5d-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2ProcessFailedEventArgs
  : public IUnknown
```

<span data-ttu-id="30f5d-107">Args de evento para o evento ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="30f5d-107">Event args for the ProcessFailed event.</span></span>

## <span data-ttu-id="30f5d-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="30f5d-108">Summary</span></span>

 <span data-ttu-id="30f5d-109">Parte</span><span class="sxs-lookup"><span data-stu-id="30f5d-109">Members</span></span>                        | <span data-ttu-id="30f5d-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="30f5d-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="30f5d-111">get_ProcessFailedKind</span><span class="sxs-lookup"><span data-stu-id="30f5d-111">get_ProcessFailedKind</span></span>](#get_processfailedkind) | <span data-ttu-id="30f5d-112">O tipo de falha de processo ocorrida.</span><span class="sxs-lookup"><span data-stu-id="30f5d-112">The kind of process failure that has occurred.</span></span>

## <span data-ttu-id="30f5d-113">Parte</span><span class="sxs-lookup"><span data-stu-id="30f5d-113">Members</span></span>

#### <span data-ttu-id="30f5d-114">get_ProcessFailedKind</span><span class="sxs-lookup"><span data-stu-id="30f5d-114">get_ProcessFailedKind</span></span> 

<span data-ttu-id="30f5d-115">O tipo de falha de processo ocorrida.</span><span class="sxs-lookup"><span data-stu-id="30f5d-115">The kind of process failure that has occurred.</span></span>

> <span data-ttu-id="30f5d-116">público HRESULT [get_ProcessFailedKind](#get_processfailedkind)(CORE_WEBVIEW2_PROCESS_FAILED_KIND \* ProcessFailedKind)</span><span class="sxs-lookup"><span data-stu-id="30f5d-116">public HRESULT [get_ProcessFailedKind](#get_processfailedkind)(CORE_WEBVIEW2_PROCESS_FAILED_KIND \* processFailedKind)</span></span>

