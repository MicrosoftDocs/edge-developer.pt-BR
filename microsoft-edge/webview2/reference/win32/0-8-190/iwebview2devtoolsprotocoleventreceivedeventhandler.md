---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.8.355-WebView2 Win32 C++ IWebView2DevToolsProtocolEventReceivedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge
ms.openlocfilehash: a26a2c18c402bffe11353b2f53f0559acde3663b
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886156"
---
# <span data-ttu-id="a3706-104">0.8.355-IWebView2DevToolsProtocolEventReceivedEventHandler de interface</span><span class="sxs-lookup"><span data-stu-id="a3706-104">0.8.355 - interface IWebView2DevToolsProtocolEventReceivedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2DevToolsProtocolEventReceivedEventHandler
  : public IUnknown
```

<span data-ttu-id="a3706-105">O chamador implementa essa interface para receber eventos DevToolsProtocolEventReceived do [IWebView2WebView](IWebView2WebView.md).</span><span class="sxs-lookup"><span data-stu-id="a3706-105">The caller implements this interface to receive DevToolsProtocolEventReceived events from the [IWebView2WebView](IWebView2WebView.md).</span></span>

## <span data-ttu-id="a3706-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="a3706-106">Summary</span></span>

 <span data-ttu-id="a3706-107">Parte</span><span class="sxs-lookup"><span data-stu-id="a3706-107">Members</span></span>                        | <span data-ttu-id="a3706-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="a3706-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="a3706-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="a3706-109">Invoke</span></span>](#invoke) | <span data-ttu-id="a3706-110">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="a3706-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="a3706-111">Parte</span><span class="sxs-lookup"><span data-stu-id="a3706-111">Members</span></span>

#### <span data-ttu-id="a3706-112">Invocar</span><span class="sxs-lookup"><span data-stu-id="a3706-112">Invoke</span></span> 

<span data-ttu-id="a3706-113">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="a3706-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="a3706-114">Public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* WebView,[IWebView2DevToolsProtocolEventReceivedEventArgs](IWebView2DevToolsProtocolEventReceivedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="a3706-114">public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* webview,[IWebView2DevToolsProtocolEventReceivedEventArgs](IWebView2DevToolsProtocolEventReceivedEventArgs.md) \* args)</span></span>

