---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: Microsoft Edge WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/09/2019
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge
ms.openlocfilehash: 602c00258e9ff3362269ebe90de8306ecbd7503e
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652405"
---
# <span data-ttu-id="7852f-104">interface IWebView2WebResourceRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="7852f-104">interface IWebView2WebResourceRequestedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="7852f-105">Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="7852f-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="7852f-106">Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.</span><span class="sxs-lookup"><span data-stu-id="7852f-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2WebResourceRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="7852f-107">Acionado quando uma solicitação HTTP é feita no WebView.</span><span class="sxs-lookup"><span data-stu-id="7852f-107">Fires when an HTTP request is made in the webview.</span></span>

## <span data-ttu-id="7852f-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="7852f-108">Summary</span></span>

 <span data-ttu-id="7852f-109">Parte</span><span class="sxs-lookup"><span data-stu-id="7852f-109">Members</span></span>                        | <span data-ttu-id="7852f-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="7852f-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="7852f-111">Invocar</span><span class="sxs-lookup"><span data-stu-id="7852f-111">Invoke</span></span>](#invoke) | <span data-ttu-id="7852f-112">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="7852f-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="7852f-113">O host pode substituir a solicitação, os cabeçalhos de resposta e o conteúdo da resposta.</span><span class="sxs-lookup"><span data-stu-id="7852f-113">The host can override request, response headers and response content.</span></span>

## <span data-ttu-id="7852f-114">Parte</span><span class="sxs-lookup"><span data-stu-id="7852f-114">Members</span></span>

#### <span data-ttu-id="7852f-115">Invocar</span><span class="sxs-lookup"><span data-stu-id="7852f-115">Invoke</span></span> 

<span data-ttu-id="7852f-116">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="7852f-116">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="7852f-117">Public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* WebView,[IWebView2WebResourceRequestedEventArgs](IWebView2WebResourceRequestedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="7852f-117">public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* webview,[IWebView2WebResourceRequestedEventArgs](IWebView2WebResourceRequestedEventArgs.md) \* args)</span></span>

