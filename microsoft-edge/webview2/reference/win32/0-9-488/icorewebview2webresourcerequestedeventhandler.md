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
ms.openlocfilehash: 2f3effd612303d1532c7220d566791a800753b37
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652388"
---
# <span data-ttu-id="08202-104">interface ICoreWebView2WebResourceRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="08202-104">interface ICoreWebView2WebResourceRequestedEventHandler</span></span> 

```
interface ICoreWebView2WebResourceRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="08202-105">Acionado quando uma solicitação HTTP é feita no WebView.</span><span class="sxs-lookup"><span data-stu-id="08202-105">Fires when an HTTP request is made in the webview.</span></span>

## <span data-ttu-id="08202-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="08202-106">Summary</span></span>

 <span data-ttu-id="08202-107">Parte</span><span class="sxs-lookup"><span data-stu-id="08202-107">Members</span></span>                        | <span data-ttu-id="08202-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="08202-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="08202-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="08202-109">Invoke</span></span>](#invoke) | <span data-ttu-id="08202-110">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="08202-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="08202-111">O host pode substituir a solicitação, os cabeçalhos de resposta e o conteúdo da resposta.</span><span class="sxs-lookup"><span data-stu-id="08202-111">The host can override request, response headers and response content.</span></span>

## <span data-ttu-id="08202-112">Parte</span><span class="sxs-lookup"><span data-stu-id="08202-112">Members</span></span>

#### <span data-ttu-id="08202-113">Invocar</span><span class="sxs-lookup"><span data-stu-id="08202-113">Invoke</span></span> 

<span data-ttu-id="08202-114">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="08202-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="08202-115">Public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* Sender, [ICoreWebView2WebResourceRequestedEventArgs](icorewebview2webresourcerequestedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="08202-115">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2WebResourceRequestedEventArgs](icorewebview2webresourcerequestedeventargs.md) \* args)</span></span>

