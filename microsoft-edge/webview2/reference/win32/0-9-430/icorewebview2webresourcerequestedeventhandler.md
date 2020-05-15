---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: Microsoft Edge WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/26/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: c4f76c468cc5001c9eae347247dd5ffb8a60594f
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652704"
---
# <span data-ttu-id="7b3e4-104">interface ICoreWebView2WebResourceRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="7b3e4-104">interface ICoreWebView2WebResourceRequestedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="7b3e4-105">Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="7b3e4-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="7b3e4-106">Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.</span><span class="sxs-lookup"><span data-stu-id="7b3e4-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2WebResourceRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="7b3e4-107">Acionado quando uma solicitação HTTP é feita no WebView.</span><span class="sxs-lookup"><span data-stu-id="7b3e4-107">Fires when an HTTP request is made in the webview.</span></span>

## <span data-ttu-id="7b3e4-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="7b3e4-108">Summary</span></span>

 <span data-ttu-id="7b3e4-109">Parte</span><span class="sxs-lookup"><span data-stu-id="7b3e4-109">Members</span></span>                        | <span data-ttu-id="7b3e4-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="7b3e4-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="7b3e4-111">Invocar</span><span class="sxs-lookup"><span data-stu-id="7b3e4-111">Invoke</span></span>](#invoke) | <span data-ttu-id="7b3e4-112">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="7b3e4-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="7b3e4-113">O host pode substituir a solicitação, os cabeçalhos de resposta e o conteúdo da resposta.</span><span class="sxs-lookup"><span data-stu-id="7b3e4-113">The host can override request, response headers and response content.</span></span>

## <span data-ttu-id="7b3e4-114">Parte</span><span class="sxs-lookup"><span data-stu-id="7b3e4-114">Members</span></span>

#### <span data-ttu-id="7b3e4-115">Invocar</span><span class="sxs-lookup"><span data-stu-id="7b3e4-115">Invoke</span></span> 

<span data-ttu-id="7b3e4-116">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="7b3e4-116">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="7b3e4-117">Public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* Sender,[ICoreWebView2WebResourceRequestedEventArgs](ICoreWebView2WebResourceRequestedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="7b3e4-117">public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* sender,[ICoreWebView2WebResourceRequestedEventArgs](ICoreWebView2WebResourceRequestedEventArgs.md) \* args)</span></span>

