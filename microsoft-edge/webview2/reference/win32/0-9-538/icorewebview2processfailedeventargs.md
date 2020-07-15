---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: WebView2 Win32 C++ ICoreWebView2ProcessFailedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2ProcessFailedEventArgs
ms.openlocfilehash: 70fb6f75594284560cb0d64663fbda47cc7404d6
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879342"
---
# <span data-ttu-id="eca29-104">interface ICoreWebView2ProcessFailedEventArgs</span><span class="sxs-lookup"><span data-stu-id="eca29-104">interface ICoreWebView2ProcessFailedEventArgs</span></span> 

```
interface ICoreWebView2ProcessFailedEventArgs
  : public IUnknown
```

<span data-ttu-id="eca29-105">Args de evento para o evento ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="eca29-105">Event args for the ProcessFailed event.</span></span>

## <span data-ttu-id="eca29-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="eca29-106">Summary</span></span>

 <span data-ttu-id="eca29-107">Parte</span><span class="sxs-lookup"><span data-stu-id="eca29-107">Members</span></span>                        | <span data-ttu-id="eca29-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="eca29-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="eca29-109">get_ProcessFailedKind</span><span class="sxs-lookup"><span data-stu-id="eca29-109">get_ProcessFailedKind</span></span>](#get_processfailedkind) | <span data-ttu-id="eca29-110">O tipo de falha de processo ocorrida.</span><span class="sxs-lookup"><span data-stu-id="eca29-110">The kind of process failure that has occurred.</span></span>

## <span data-ttu-id="eca29-111">Parte</span><span class="sxs-lookup"><span data-stu-id="eca29-111">Members</span></span>

#### <span data-ttu-id="eca29-112">get_ProcessFailedKind</span><span class="sxs-lookup"><span data-stu-id="eca29-112">get_ProcessFailedKind</span></span> 

<span data-ttu-id="eca29-113">O tipo de falha de processo ocorrida.</span><span class="sxs-lookup"><span data-stu-id="eca29-113">The kind of process failure that has occurred.</span></span>

> <span data-ttu-id="eca29-114">público HRESULT [get_ProcessFailedKind](#get_processfailedkind)(COREWEBVIEW2_PROCESS_FAILED_KIND \* ProcessFailedKind)</span><span class="sxs-lookup"><span data-stu-id="eca29-114">public HRESULT [get_ProcessFailedKind](#get_processfailedkind)(COREWEBVIEW2_PROCESS_FAILED_KIND \* processFailedKind)</span></span>

