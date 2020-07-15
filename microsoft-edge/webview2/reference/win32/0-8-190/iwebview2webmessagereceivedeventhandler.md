---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.8.355-WebView2 Win32 C++ IWebView2WebMessageReceivedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge
ms.openlocfilehash: 55ce9b2efc78bd4f0bf153c1e5655ff79d42af94
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878152"
---
# <span data-ttu-id="72ed9-104">0.8.355-IWebView2WebMessageReceivedEventHandler de interface</span><span class="sxs-lookup"><span data-stu-id="72ed9-104">0.8.355 - interface IWebView2WebMessageReceivedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="72ed9-105">Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="72ed9-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="72ed9-106">Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.</span><span class="sxs-lookup"><span data-stu-id="72ed9-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2WebMessageReceivedEventHandler
  : public IUnknown
```

<span data-ttu-id="72ed9-107">O chamador implementa essa interface para receber o evento WebMessageReceived.</span><span class="sxs-lookup"><span data-stu-id="72ed9-107">The caller implements this interface to receive the WebMessageReceived event.</span></span>

## <span data-ttu-id="72ed9-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="72ed9-108">Summary</span></span>

 <span data-ttu-id="72ed9-109">Parte</span><span class="sxs-lookup"><span data-stu-id="72ed9-109">Members</span></span>                        | <span data-ttu-id="72ed9-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="72ed9-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="72ed9-111">Invocar</span><span class="sxs-lookup"><span data-stu-id="72ed9-111">Invoke</span></span>](#invoke) | <span data-ttu-id="72ed9-112">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="72ed9-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="72ed9-113">Parte</span><span class="sxs-lookup"><span data-stu-id="72ed9-113">Members</span></span>

#### <span data-ttu-id="72ed9-114">Invocar</span><span class="sxs-lookup"><span data-stu-id="72ed9-114">Invoke</span></span> 

<span data-ttu-id="72ed9-115">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="72ed9-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="72ed9-116">Public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* WebView,[IWebView2WebMessageReceivedEventArgs](IWebView2WebMessageReceivedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="72ed9-116">public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* webview,[IWebView2WebMessageReceivedEventArgs](IWebView2WebMessageReceivedEventArgs.md) \* args)</span></span>

