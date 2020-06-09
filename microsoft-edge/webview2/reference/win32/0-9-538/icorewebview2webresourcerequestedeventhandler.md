---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: Microsoft Edge WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: 64f29f8c771a14d569fd45f7359614795bbc0386
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698380"
---
# <span data-ttu-id="ecc8b-104">interface ICoreWebView2WebResourceRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="ecc8b-104">interface ICoreWebView2WebResourceRequestedEventHandler</span></span> 

```
interface ICoreWebView2WebResourceRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="ecc8b-105">Acionado quando uma solicitação HTTP é feita no WebView.</span><span class="sxs-lookup"><span data-stu-id="ecc8b-105">Fires when an HTTP request is made in the webview.</span></span>

## <span data-ttu-id="ecc8b-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="ecc8b-106">Summary</span></span>

 <span data-ttu-id="ecc8b-107">Parte</span><span class="sxs-lookup"><span data-stu-id="ecc8b-107">Members</span></span>                        | <span data-ttu-id="ecc8b-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="ecc8b-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="ecc8b-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="ecc8b-109">Invoke</span></span>](#invoke) | <span data-ttu-id="ecc8b-110">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="ecc8b-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="ecc8b-111">O host pode substituir a solicitação, os cabeçalhos de resposta e o conteúdo da resposta.</span><span class="sxs-lookup"><span data-stu-id="ecc8b-111">The host can override request, response headers and response content.</span></span>

## <span data-ttu-id="ecc8b-112">Parte</span><span class="sxs-lookup"><span data-stu-id="ecc8b-112">Members</span></span>

#### <span data-ttu-id="ecc8b-113">Invocar</span><span class="sxs-lookup"><span data-stu-id="ecc8b-113">Invoke</span></span> 

<span data-ttu-id="ecc8b-114">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="ecc8b-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="ecc8b-115">Public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* Sender, [ICoreWebView2WebResourceRequestedEventArgs](icorewebview2webresourcerequestedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="ecc8b-115">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2WebResourceRequestedEventArgs](icorewebview2webresourcerequestedeventargs.md) \* args)</span></span>

