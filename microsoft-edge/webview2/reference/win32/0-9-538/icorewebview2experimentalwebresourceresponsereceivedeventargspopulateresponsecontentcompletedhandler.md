---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: WebView2 Win32 C++ ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgsPopulateResponseContentCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgsPopulateResponseContentCompletedHandler
ms.openlocfilehash: c021cfa866e55bfdf30185eeaf6015db1b523271
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886505"
---
# <span data-ttu-id="e4bca-104">interface ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgsPopulateResponseContentCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="e4bca-104">interface ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgsPopulateResponseContentCompletedHandler</span></span> 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

```
interface ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgsPopulateResponseContentCompletedHandler
  : public IUnknown
```

<span data-ttu-id="e4bca-105">Manipulador de conclusão para PopulateResponseContent método Async.</span><span class="sxs-lookup"><span data-stu-id="e4bca-105">Completion handler for PopulateResponseContent async method.</span></span>

## <span data-ttu-id="e4bca-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="e4bca-106">Summary</span></span>

 <span data-ttu-id="e4bca-107">Parte</span><span class="sxs-lookup"><span data-stu-id="e4bca-107">Members</span></span>                        | <span data-ttu-id="e4bca-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="e4bca-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="e4bca-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="e4bca-109">Invoke</span></span>](#invoke) | <span data-ttu-id="e4bca-110">Chamado para fornecer o implementador com o status de conclusão da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="e4bca-110">Called to provide the implementer with the completion status of the corresponding asynchronous method call.</span></span>

<span data-ttu-id="e4bca-111">Ele é invocado quando o fluxo de conteúdo da resposta de um evento WebResourceResponseReceieved está disponível.</span><span class="sxs-lookup"><span data-stu-id="e4bca-111">It's invoked when the Content stream of the Response of a WebResourceResponseReceieved event is available.</span></span>

## <span data-ttu-id="e4bca-112">Parte</span><span class="sxs-lookup"><span data-stu-id="e4bca-112">Members</span></span>

#### <span data-ttu-id="e4bca-113">Invocar</span><span class="sxs-lookup"><span data-stu-id="e4bca-113">Invoke</span></span> 

<span data-ttu-id="e4bca-114">Chamado para fornecer o implementador com o status de conclusão da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="e4bca-114">Called to provide the implementer with the completion status of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="e4bca-115">[chamada](#invoke)a Public HRESULT (resultado HRESULT)</span><span class="sxs-lookup"><span data-stu-id="e4bca-115">public HRESULT [Invoke](#invoke)(HRESULT result)</span></span>

