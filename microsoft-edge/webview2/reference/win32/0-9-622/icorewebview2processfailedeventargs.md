---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: WebView2 Win32 C++ ICoreWebView2ProcessFailedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2ProcessFailedEventArgs
ms.openlocfilehash: 0f4ce5d4922b7a721ce2652fadfa5169a52cb458
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011557"
---
# <span data-ttu-id="5f892-104">interface ICoreWebView2ProcessFailedEventArgs</span><span class="sxs-lookup"><span data-stu-id="5f892-104">interface ICoreWebView2ProcessFailedEventArgs</span></span> 

```
interface ICoreWebView2ProcessFailedEventArgs
  : public IUnknown
```

<span data-ttu-id="5f892-105">Args de evento para o evento ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="5f892-105">Event args for the ProcessFailed event.</span></span>

## <span data-ttu-id="5f892-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="5f892-106">Summary</span></span>

 <span data-ttu-id="5f892-107">Parte</span><span class="sxs-lookup"><span data-stu-id="5f892-107">Members</span></span>                        | <span data-ttu-id="5f892-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="5f892-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="5f892-109">get_ProcessFailedKind</span><span class="sxs-lookup"><span data-stu-id="5f892-109">get_ProcessFailedKind</span></span>](#get_processfailedkind) | <span data-ttu-id="5f892-110">O tipo de falha de processo ocorrida.</span><span class="sxs-lookup"><span data-stu-id="5f892-110">The kind of process failure that has occurred.</span></span>

## <span data-ttu-id="5f892-111">Parte</span><span class="sxs-lookup"><span data-stu-id="5f892-111">Members</span></span>

#### <span data-ttu-id="5f892-112">get_ProcessFailedKind</span><span class="sxs-lookup"><span data-stu-id="5f892-112">get_ProcessFailedKind</span></span> 

<span data-ttu-id="5f892-113">O tipo de falha de processo ocorrida.</span><span class="sxs-lookup"><span data-stu-id="5f892-113">The kind of process failure that has occurred.</span></span>

> <span data-ttu-id="5f892-114">público HRESULT [get_ProcessFailedKind](#get_processfailedkind)(COREWEBVIEW2_PROCESS_FAILED_KIND \* ProcessFailedKind)</span><span class="sxs-lookup"><span data-stu-id="5f892-114">public HRESULT [get_ProcessFailedKind](#get_processfailedkind)(COREWEBVIEW2_PROCESS_FAILED_KIND \* processFailedKind)</span></span>

