---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.8.355-WebView2 Win32 C++ IWebView2ProcessFailedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge
ms.openlocfilehash: 697a49bfe68f83085f6c961ee2cdd5ab21f3b59b
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885818"
---
# <span data-ttu-id="f033f-104">0.8.355-IWebView2ProcessFailedEventArgs de interface</span><span class="sxs-lookup"><span data-stu-id="f033f-104">0.8.355 - interface IWebView2ProcessFailedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2ProcessFailedEventArgs
  : public IUnknown
```

<span data-ttu-id="f033f-105">Args de evento para o evento ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="f033f-105">Event args for the ProcessFailed event.</span></span>

## <span data-ttu-id="f033f-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="f033f-106">Summary</span></span>

 <span data-ttu-id="f033f-107">Parte</span><span class="sxs-lookup"><span data-stu-id="f033f-107">Members</span></span>                        | <span data-ttu-id="f033f-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="f033f-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="f033f-109">get_ProcessFailedKind</span><span class="sxs-lookup"><span data-stu-id="f033f-109">get_ProcessFailedKind</span></span>](#get_processfailedkind) | <span data-ttu-id="f033f-110">O tipo de falha de processo ocorrida.</span><span class="sxs-lookup"><span data-stu-id="f033f-110">The kind of process failure that has occurred.</span></span>

## <span data-ttu-id="f033f-111">Parte</span><span class="sxs-lookup"><span data-stu-id="f033f-111">Members</span></span>

#### <span data-ttu-id="f033f-112">get_ProcessFailedKind</span><span class="sxs-lookup"><span data-stu-id="f033f-112">get_ProcessFailedKind</span></span> 

<span data-ttu-id="f033f-113">O tipo de falha de processo ocorrida.</span><span class="sxs-lookup"><span data-stu-id="f033f-113">The kind of process failure that has occurred.</span></span>

> <span data-ttu-id="f033f-114">público HRESULT [get_ProcessFailedKind](#get_processfailedkind)(WEBVIEW2_PROCESS_FAILED_KIND \* ProcessFailedKind)</span><span class="sxs-lookup"><span data-stu-id="f033f-114">public HRESULT [get_ProcessFailedKind](#get_processfailedkind)(WEBVIEW2_PROCESS_FAILED_KIND \* processFailedKind)</span></span>

