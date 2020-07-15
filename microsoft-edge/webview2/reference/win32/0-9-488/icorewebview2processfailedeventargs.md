---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2ProcessFailedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: ac3b1fc5ceb31cbf2d67649b91f3bfbf2c8ecbe3
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880364"
---
# <span data-ttu-id="819a7-104">0.9.515-ICoreWebView2ProcessFailedEventArgs de interface</span><span class="sxs-lookup"><span data-stu-id="819a7-104">0.9.515 - interface ICoreWebView2ProcessFailedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="819a7-105">Esta referência pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="819a7-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="819a7-106">Consulte a [referência de API WebView2](../../../webview2-api-reference.md) para obter a referência de API mais recente.</span><span class="sxs-lookup"><span data-stu-id="819a7-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2ProcessFailedEventArgs
  : public IUnknown
```

<span data-ttu-id="819a7-107">Args de evento para o evento ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="819a7-107">Event args for the ProcessFailed event.</span></span>

## <span data-ttu-id="819a7-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="819a7-108">Summary</span></span>

 <span data-ttu-id="819a7-109">Parte</span><span class="sxs-lookup"><span data-stu-id="819a7-109">Members</span></span>                        | <span data-ttu-id="819a7-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="819a7-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="819a7-111">get_ProcessFailedKind</span><span class="sxs-lookup"><span data-stu-id="819a7-111">get_ProcessFailedKind</span></span>](#get_processfailedkind) | <span data-ttu-id="819a7-112">O tipo de falha de processo ocorrida.</span><span class="sxs-lookup"><span data-stu-id="819a7-112">The kind of process failure that has occurred.</span></span>

## <span data-ttu-id="819a7-113">Parte</span><span class="sxs-lookup"><span data-stu-id="819a7-113">Members</span></span>

#### <span data-ttu-id="819a7-114">get_ProcessFailedKind</span><span class="sxs-lookup"><span data-stu-id="819a7-114">get_ProcessFailedKind</span></span> 

<span data-ttu-id="819a7-115">O tipo de falha de processo ocorrida.</span><span class="sxs-lookup"><span data-stu-id="819a7-115">The kind of process failure that has occurred.</span></span>

> <span data-ttu-id="819a7-116">público HRESULT [get_ProcessFailedKind](#get_processfailedkind)(COREWEBVIEW2_PROCESS_FAILED_KIND \* ProcessFailedKind)</span><span class="sxs-lookup"><span data-stu-id="819a7-116">public HRESULT [get_ProcessFailedKind](#get_processfailedkind)(COREWEBVIEW2_PROCESS_FAILED_KIND \* processFailedKind)</span></span>

