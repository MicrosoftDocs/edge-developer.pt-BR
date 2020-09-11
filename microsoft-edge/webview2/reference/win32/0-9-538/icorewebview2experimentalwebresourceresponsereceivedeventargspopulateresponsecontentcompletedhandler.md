---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgsPopulateResponseContentCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgsPopulateResponseContentCompletedHandler
ms.openlocfilehash: 6a854eb9ca73f45e366edfa144c273f780bcee94
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011409"
---
# <span data-ttu-id="3d54c-104">0.9.579-ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgsPopulateResponseContentCompletedHandler de interface</span><span class="sxs-lookup"><span data-stu-id="3d54c-104">0.9.579 - interface ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgsPopulateResponseContentCompletedHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

```
interface ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgsPopulateResponseContentCompletedHandler
  : public IUnknown
```

<span data-ttu-id="3d54c-105">Manipulador de conclusão para PopulateResponseContent método Async.</span><span class="sxs-lookup"><span data-stu-id="3d54c-105">Completion handler for PopulateResponseContent async method.</span></span>

## <span data-ttu-id="3d54c-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="3d54c-106">Summary</span></span>

 <span data-ttu-id="3d54c-107">Parte</span><span class="sxs-lookup"><span data-stu-id="3d54c-107">Members</span></span>                        | <span data-ttu-id="3d54c-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="3d54c-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="3d54c-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="3d54c-109">Invoke</span></span>](#invoke) | <span data-ttu-id="3d54c-110">Chamado para fornecer o implementador com o status de conclusão da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="3d54c-110">Called to provide the implementer with the completion status of the corresponding asynchronous method call.</span></span>

<span data-ttu-id="3d54c-111">Ele é invocado quando o fluxo de conteúdo da resposta de um evento WebResourceResponseReceieved está disponível.</span><span class="sxs-lookup"><span data-stu-id="3d54c-111">It's invoked when the Content stream of the Response of a WebResourceResponseReceieved event is available.</span></span>

## <span data-ttu-id="3d54c-112">Parte</span><span class="sxs-lookup"><span data-stu-id="3d54c-112">Members</span></span>

#### <span data-ttu-id="3d54c-113">Invocar</span><span class="sxs-lookup"><span data-stu-id="3d54c-113">Invoke</span></span> 

<span data-ttu-id="3d54c-114">Chamado para fornecer o implementador com o status de conclusão da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="3d54c-114">Called to provide the implementer with the completion status of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="3d54c-115">[chamada](#invoke)a Public HRESULT (resultado HRESULT)</span><span class="sxs-lookup"><span data-stu-id="3d54c-115">public HRESULT [Invoke](#invoke)(HRESULT result)</span></span>

