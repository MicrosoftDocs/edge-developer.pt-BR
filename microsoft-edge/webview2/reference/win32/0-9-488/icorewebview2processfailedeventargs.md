---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: Microsoft Edge WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/16/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: 4183f3a1c60bd9e2bdcff5227426db1f07c313cf
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697515"
---
# <span data-ttu-id="96c06-104">interface ICoreWebView2ProcessFailedEventArgs</span><span class="sxs-lookup"><span data-stu-id="96c06-104">interface ICoreWebView2ProcessFailedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="96c06-105">Esta referência pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="96c06-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="96c06-106">Consulte a [referência de API WebView2](../../../webview2-api-reference.md) para obter a referência de API mais recente.</span><span class="sxs-lookup"><span data-stu-id="96c06-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2ProcessFailedEventArgs
  : public IUnknown
```

<span data-ttu-id="96c06-107">Args de evento para o evento ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="96c06-107">Event args for the ProcessFailed event.</span></span>

## <span data-ttu-id="96c06-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="96c06-108">Summary</span></span>

 <span data-ttu-id="96c06-109">Parte</span><span class="sxs-lookup"><span data-stu-id="96c06-109">Members</span></span>                        | <span data-ttu-id="96c06-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="96c06-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="96c06-111">get_ProcessFailedKind</span><span class="sxs-lookup"><span data-stu-id="96c06-111">get_ProcessFailedKind</span></span>](#get_processfailedkind) | <span data-ttu-id="96c06-112">O tipo de falha de processo ocorrida.</span><span class="sxs-lookup"><span data-stu-id="96c06-112">The kind of process failure that has occurred.</span></span>

## <span data-ttu-id="96c06-113">Parte</span><span class="sxs-lookup"><span data-stu-id="96c06-113">Members</span></span>

#### <span data-ttu-id="96c06-114">get_ProcessFailedKind</span><span class="sxs-lookup"><span data-stu-id="96c06-114">get_ProcessFailedKind</span></span> 

<span data-ttu-id="96c06-115">O tipo de falha de processo ocorrida.</span><span class="sxs-lookup"><span data-stu-id="96c06-115">The kind of process failure that has occurred.</span></span>

> <span data-ttu-id="96c06-116">público HRESULT [get_ProcessFailedKind](#get_processfailedkind)(COREWEBVIEW2_PROCESS_FAILED_KIND \* ProcessFailedKind)</span><span class="sxs-lookup"><span data-stu-id="96c06-116">public HRESULT [get_ProcessFailedKind](#get_processfailedkind)(COREWEBVIEW2_PROCESS_FAILED_KIND \* processFailedKind)</span></span>

