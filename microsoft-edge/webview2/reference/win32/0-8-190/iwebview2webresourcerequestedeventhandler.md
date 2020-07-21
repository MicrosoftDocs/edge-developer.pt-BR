---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.8.355-WebView2 Win32 C++ IWebView2WebResourceRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge
ms.openlocfilehash: 70ecc1898f9a72656f12b912d103116c381d4218
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885671"
---
# <span data-ttu-id="51f38-104">0.8.355-IWebView2WebResourceRequestedEventHandler de interface</span><span class="sxs-lookup"><span data-stu-id="51f38-104">0.8.355 - interface IWebView2WebResourceRequestedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2WebResourceRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="51f38-105">Acionado quando uma solicitação HTTP é feita no WebView.</span><span class="sxs-lookup"><span data-stu-id="51f38-105">Fires when an HTTP request is made in the webview.</span></span>

## <span data-ttu-id="51f38-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="51f38-106">Summary</span></span>

 <span data-ttu-id="51f38-107">Parte</span><span class="sxs-lookup"><span data-stu-id="51f38-107">Members</span></span>                        | <span data-ttu-id="51f38-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="51f38-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="51f38-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="51f38-109">Invoke</span></span>](#invoke) | <span data-ttu-id="51f38-110">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="51f38-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="51f38-111">O host pode substituir a solicitação, os cabeçalhos de resposta e o conteúdo da resposta.</span><span class="sxs-lookup"><span data-stu-id="51f38-111">The host can override request, response headers and response content.</span></span>

## <span data-ttu-id="51f38-112">Parte</span><span class="sxs-lookup"><span data-stu-id="51f38-112">Members</span></span>

#### <span data-ttu-id="51f38-113">Invocar</span><span class="sxs-lookup"><span data-stu-id="51f38-113">Invoke</span></span> 

<span data-ttu-id="51f38-114">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="51f38-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="51f38-115">Public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* WebView,[IWebView2WebResourceRequestedEventArgs](IWebView2WebResourceRequestedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="51f38-115">public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* webview,[IWebView2WebResourceRequestedEventArgs](IWebView2WebResourceRequestedEventArgs.md) \* args)</span></span>

