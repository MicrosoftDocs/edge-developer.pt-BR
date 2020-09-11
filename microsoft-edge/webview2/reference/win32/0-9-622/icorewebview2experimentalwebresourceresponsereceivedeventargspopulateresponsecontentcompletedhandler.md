---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: WebView2 Win32 C++ ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgsPopulateResponseContentCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgsPopulateResponseContentCompletedHandler
ms.openlocfilehash: 6c97e0591d55570f4076f6a5c4f2eebc2cc7c5ad
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011448"
---
# <span data-ttu-id="f5902-104">interface ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgsPopulateResponseContentCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="f5902-104">interface ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgsPopulateResponseContentCompletedHandler</span></span> 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

```
interface ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgsPopulateResponseContentCompletedHandler
  : public IUnknown
```

<span data-ttu-id="f5902-105">Manipulador de conclusão para PopulateResponseContent método Async.</span><span class="sxs-lookup"><span data-stu-id="f5902-105">Completion handler for PopulateResponseContent async method.</span></span>

## <span data-ttu-id="f5902-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="f5902-106">Summary</span></span>

 <span data-ttu-id="f5902-107">Parte</span><span class="sxs-lookup"><span data-stu-id="f5902-107">Members</span></span>                        | <span data-ttu-id="f5902-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="f5902-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="f5902-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="f5902-109">Invoke</span></span>](#invoke) | <span data-ttu-id="f5902-110">Chamado para fornecer o implementador com o status de conclusão da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="f5902-110">Called to provide the implementer with the completion status of the corresponding asynchronous method call.</span></span>

<span data-ttu-id="f5902-111">Ele é invocado quando o fluxo de conteúdo da resposta de um evento WebResourceResponseReceieved está disponível.</span><span class="sxs-lookup"><span data-stu-id="f5902-111">It's invoked when the Content stream of the Response of a WebResourceResponseReceieved event is available.</span></span>

## <span data-ttu-id="f5902-112">Parte</span><span class="sxs-lookup"><span data-stu-id="f5902-112">Members</span></span>

#### <span data-ttu-id="f5902-113">Invocar</span><span class="sxs-lookup"><span data-stu-id="f5902-113">Invoke</span></span> 

<span data-ttu-id="f5902-114">Chamado para fornecer o implementador com o status de conclusão da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="f5902-114">Called to provide the implementer with the completion status of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="f5902-115">[chamada](#invoke)a Public HRESULT (HRESULT ErrorCode)</span><span class="sxs-lookup"><span data-stu-id="f5902-115">public HRESULT [Invoke](#invoke)(HRESULT errorCode)</span></span>

