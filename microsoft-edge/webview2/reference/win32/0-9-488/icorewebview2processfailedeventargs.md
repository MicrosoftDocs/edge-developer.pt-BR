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
ms.openlocfilehash: 0efc1656b8204b9775002db49e0e4a5734682cc4
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652361"
---
# <span data-ttu-id="d7bc8-104">interface ICoreWebView2ProcessFailedEventArgs</span><span class="sxs-lookup"><span data-stu-id="d7bc8-104">interface ICoreWebView2ProcessFailedEventArgs</span></span> 

```
interface ICoreWebView2ProcessFailedEventArgs
  : public IUnknown
```

<span data-ttu-id="d7bc8-105">Args de evento para o evento ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="d7bc8-105">Event args for the ProcessFailed event.</span></span>

## <span data-ttu-id="d7bc8-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="d7bc8-106">Summary</span></span>

 <span data-ttu-id="d7bc8-107">Parte</span><span class="sxs-lookup"><span data-stu-id="d7bc8-107">Members</span></span>                        | <span data-ttu-id="d7bc8-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="d7bc8-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="d7bc8-109">get_ProcessFailedKind</span><span class="sxs-lookup"><span data-stu-id="d7bc8-109">get_ProcessFailedKind</span></span>](#get_processfailedkind) | <span data-ttu-id="d7bc8-110">O tipo de falha de processo ocorrida.</span><span class="sxs-lookup"><span data-stu-id="d7bc8-110">The kind of process failure that has occurred.</span></span>

## <span data-ttu-id="d7bc8-111">Parte</span><span class="sxs-lookup"><span data-stu-id="d7bc8-111">Members</span></span>

#### <span data-ttu-id="d7bc8-112">get_ProcessFailedKind</span><span class="sxs-lookup"><span data-stu-id="d7bc8-112">get_ProcessFailedKind</span></span> 

<span data-ttu-id="d7bc8-113">O tipo de falha de processo ocorrida.</span><span class="sxs-lookup"><span data-stu-id="d7bc8-113">The kind of process failure that has occurred.</span></span>

> <span data-ttu-id="d7bc8-114">público HRESULT [get_ProcessFailedKind](#get_processfailedkind)(COREWEBVIEW2_PROCESS_FAILED_KIND \* ProcessFailedKind)</span><span class="sxs-lookup"><span data-stu-id="d7bc8-114">public HRESULT [get_ProcessFailedKind](#get_processfailedkind)(COREWEBVIEW2_PROCESS_FAILED_KIND \* processFailedKind)</span></span>

