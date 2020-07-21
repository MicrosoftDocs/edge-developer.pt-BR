---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2WebResourceRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: d35e21fde7788b1df5b201f8690196ecd0d82a34
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884084"
---
# <span data-ttu-id="04c3d-104">0.9.430-ICoreWebView2WebResourceRequestedEventHandler de interface</span><span class="sxs-lookup"><span data-stu-id="04c3d-104">0.9.430 - interface ICoreWebView2WebResourceRequestedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2WebResourceRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="04c3d-105">Acionado quando uma solicitação HTTP é feita no WebView.</span><span class="sxs-lookup"><span data-stu-id="04c3d-105">Fires when an HTTP request is made in the webview.</span></span>

## <span data-ttu-id="04c3d-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="04c3d-106">Summary</span></span>

 <span data-ttu-id="04c3d-107">Parte</span><span class="sxs-lookup"><span data-stu-id="04c3d-107">Members</span></span>                        | <span data-ttu-id="04c3d-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="04c3d-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="04c3d-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="04c3d-109">Invoke</span></span>](#invoke) | <span data-ttu-id="04c3d-110">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="04c3d-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="04c3d-111">O host pode substituir a solicitação, os cabeçalhos de resposta e o conteúdo da resposta.</span><span class="sxs-lookup"><span data-stu-id="04c3d-111">The host can override request, response headers and response content.</span></span>

## <span data-ttu-id="04c3d-112">Parte</span><span class="sxs-lookup"><span data-stu-id="04c3d-112">Members</span></span>

#### <span data-ttu-id="04c3d-113">Invocar</span><span class="sxs-lookup"><span data-stu-id="04c3d-113">Invoke</span></span> 

<span data-ttu-id="04c3d-114">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="04c3d-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="04c3d-115">Public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* Sender,[ICoreWebView2WebResourceRequestedEventArgs](ICoreWebView2WebResourceRequestedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="04c3d-115">public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* sender,[ICoreWebView2WebResourceRequestedEventArgs](ICoreWebView2WebResourceRequestedEventArgs.md) \* args)</span></span>

