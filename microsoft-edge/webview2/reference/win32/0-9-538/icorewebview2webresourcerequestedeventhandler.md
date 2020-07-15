---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: WebView2 Win32 C++ ICoreWebView2WebResourceRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2WebResourceRequestedEventHandler
ms.openlocfilehash: 9cd221ac1b528b0be52201daa0c15217534944a6
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879223"
---
# <span data-ttu-id="3ab5a-104">interface ICoreWebView2WebResourceRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="3ab5a-104">interface ICoreWebView2WebResourceRequestedEventHandler</span></span> 

```
interface ICoreWebView2WebResourceRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="3ab5a-105">Acionado quando uma solicitação HTTP é feita no WebView.</span><span class="sxs-lookup"><span data-stu-id="3ab5a-105">Fires when an HTTP request is made in the webview.</span></span>

## <span data-ttu-id="3ab5a-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="3ab5a-106">Summary</span></span>

 <span data-ttu-id="3ab5a-107">Parte</span><span class="sxs-lookup"><span data-stu-id="3ab5a-107">Members</span></span>                        | <span data-ttu-id="3ab5a-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="3ab5a-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="3ab5a-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="3ab5a-109">Invoke</span></span>](#invoke) | <span data-ttu-id="3ab5a-110">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="3ab5a-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="3ab5a-111">O host pode substituir a solicitação, os cabeçalhos de resposta e o conteúdo da resposta.</span><span class="sxs-lookup"><span data-stu-id="3ab5a-111">The host can override request, response headers and response content.</span></span>

## <span data-ttu-id="3ab5a-112">Parte</span><span class="sxs-lookup"><span data-stu-id="3ab5a-112">Members</span></span>

#### <span data-ttu-id="3ab5a-113">Invocar</span><span class="sxs-lookup"><span data-stu-id="3ab5a-113">Invoke</span></span> 

<span data-ttu-id="3ab5a-114">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="3ab5a-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="3ab5a-115">Public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* Sender, [ICoreWebView2WebResourceRequestedEventArgs](icorewebview2webresourcerequestedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="3ab5a-115">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2WebResourceRequestedEventArgs](icorewebview2webresourcerequestedeventargs.md) \* args)</span></span>

