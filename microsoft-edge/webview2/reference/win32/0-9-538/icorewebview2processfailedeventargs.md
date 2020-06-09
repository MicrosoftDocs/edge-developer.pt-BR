---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: Microsoft Edge WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: c01d98ca997a0b4e288ecaa8ede609c93fc84ea1
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698260"
---
# <span data-ttu-id="063f5-104">interface ICoreWebView2ProcessFailedEventArgs</span><span class="sxs-lookup"><span data-stu-id="063f5-104">interface ICoreWebView2ProcessFailedEventArgs</span></span> 

```
interface ICoreWebView2ProcessFailedEventArgs
  : public IUnknown
```

<span data-ttu-id="063f5-105">Args de evento para o evento ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="063f5-105">Event args for the ProcessFailed event.</span></span>

## <span data-ttu-id="063f5-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="063f5-106">Summary</span></span>

 <span data-ttu-id="063f5-107">Parte</span><span class="sxs-lookup"><span data-stu-id="063f5-107">Members</span></span>                        | <span data-ttu-id="063f5-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="063f5-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="063f5-109">get_ProcessFailedKind</span><span class="sxs-lookup"><span data-stu-id="063f5-109">get_ProcessFailedKind</span></span>](#get_processfailedkind) | <span data-ttu-id="063f5-110">O tipo de falha de processo ocorrida.</span><span class="sxs-lookup"><span data-stu-id="063f5-110">The kind of process failure that has occurred.</span></span>

## <span data-ttu-id="063f5-111">Parte</span><span class="sxs-lookup"><span data-stu-id="063f5-111">Members</span></span>

#### <span data-ttu-id="063f5-112">get_ProcessFailedKind</span><span class="sxs-lookup"><span data-stu-id="063f5-112">get_ProcessFailedKind</span></span> 

<span data-ttu-id="063f5-113">O tipo de falha de processo ocorrida.</span><span class="sxs-lookup"><span data-stu-id="063f5-113">The kind of process failure that has occurred.</span></span>

> <span data-ttu-id="063f5-114">público HRESULT [get_ProcessFailedKind](#get_processfailedkind)(COREWEBVIEW2_PROCESS_FAILED_KIND \* ProcessFailedKind)</span><span class="sxs-lookup"><span data-stu-id="063f5-114">public HRESULT [get_ProcessFailedKind](#get_processfailedkind)(COREWEBVIEW2_PROCESS_FAILED_KIND \* processFailedKind)</span></span>

