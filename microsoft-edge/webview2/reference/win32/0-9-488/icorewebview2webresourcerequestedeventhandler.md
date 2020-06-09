---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: Microsoft Edge WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/07/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: 622a7e93912a3380cc0d7dabae9293734cd3fcfa
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697935"
---
# <span data-ttu-id="c80a3-104">interface ICoreWebView2WebResourceRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="c80a3-104">interface ICoreWebView2WebResourceRequestedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="c80a3-105">Esta referência pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="c80a3-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="c80a3-106">Consulte a [referência de API WebView2](../../../webview2-api-reference.md) para obter a referência de API mais recente.</span><span class="sxs-lookup"><span data-stu-id="c80a3-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2WebResourceRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="c80a3-107">Acionado quando uma solicitação HTTP é feita no WebView.</span><span class="sxs-lookup"><span data-stu-id="c80a3-107">Fires when an HTTP request is made in the webview.</span></span>

## <span data-ttu-id="c80a3-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="c80a3-108">Summary</span></span>

 <span data-ttu-id="c80a3-109">Parte</span><span class="sxs-lookup"><span data-stu-id="c80a3-109">Members</span></span>                        | <span data-ttu-id="c80a3-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="c80a3-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="c80a3-111">Invocar</span><span class="sxs-lookup"><span data-stu-id="c80a3-111">Invoke</span></span>](#invoke) | <span data-ttu-id="c80a3-112">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="c80a3-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="c80a3-113">O host pode substituir a solicitação, os cabeçalhos de resposta e o conteúdo da resposta.</span><span class="sxs-lookup"><span data-stu-id="c80a3-113">The host can override request, response headers and response content.</span></span>

## <span data-ttu-id="c80a3-114">Parte</span><span class="sxs-lookup"><span data-stu-id="c80a3-114">Members</span></span>

#### <span data-ttu-id="c80a3-115">Invocar</span><span class="sxs-lookup"><span data-stu-id="c80a3-115">Invoke</span></span> 

<span data-ttu-id="c80a3-116">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="c80a3-116">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="c80a3-117">Public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* Sender, [ICoreWebView2WebResourceRequestedEventArgs](icorewebview2webresourcerequestedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="c80a3-117">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2WebResourceRequestedEventArgs](icorewebview2webresourcerequestedeventargs.md) \* args)</span></span>

