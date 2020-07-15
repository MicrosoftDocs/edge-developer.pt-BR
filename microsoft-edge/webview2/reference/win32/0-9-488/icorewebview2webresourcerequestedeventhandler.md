---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2WebResourceRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: 715af5cbf2bbaf8301e39dce1516019102b61ab1
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877326"
---
# <span data-ttu-id="f348b-104">0.9.515-ICoreWebView2WebResourceRequestedEventHandler de interface</span><span class="sxs-lookup"><span data-stu-id="f348b-104">0.9.515 - interface ICoreWebView2WebResourceRequestedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="f348b-105">Esta referência pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="f348b-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="f348b-106">Consulte a [referência de API WebView2](../../../webview2-api-reference.md) para obter a referência de API mais recente.</span><span class="sxs-lookup"><span data-stu-id="f348b-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2WebResourceRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="f348b-107">Acionado quando uma solicitação HTTP é feita no WebView.</span><span class="sxs-lookup"><span data-stu-id="f348b-107">Fires when an HTTP request is made in the webview.</span></span>

## <span data-ttu-id="f348b-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="f348b-108">Summary</span></span>

 <span data-ttu-id="f348b-109">Parte</span><span class="sxs-lookup"><span data-stu-id="f348b-109">Members</span></span>                        | <span data-ttu-id="f348b-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="f348b-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="f348b-111">Invocar</span><span class="sxs-lookup"><span data-stu-id="f348b-111">Invoke</span></span>](#invoke) | <span data-ttu-id="f348b-112">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="f348b-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="f348b-113">O host pode substituir a solicitação, os cabeçalhos de resposta e o conteúdo da resposta.</span><span class="sxs-lookup"><span data-stu-id="f348b-113">The host can override request, response headers and response content.</span></span>

## <span data-ttu-id="f348b-114">Parte</span><span class="sxs-lookup"><span data-stu-id="f348b-114">Members</span></span>

#### <span data-ttu-id="f348b-115">Invocar</span><span class="sxs-lookup"><span data-stu-id="f348b-115">Invoke</span></span> 

<span data-ttu-id="f348b-116">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="f348b-116">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="f348b-117">Public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* Sender, [ICoreWebView2WebResourceRequestedEventArgs](icorewebview2webresourcerequestedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="f348b-117">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2WebResourceRequestedEventArgs](icorewebview2webresourcerequestedeventargs.md) \* args)</span></span>

