---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2DevToolsProtocolEventReceivedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: c08a851eb21947cae4af465a233dc4c49508c84c
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884208"
---
# <span data-ttu-id="5dd2e-104">0.9.430-ICoreWebView2DevToolsProtocolEventReceivedEventHandler de interface</span><span class="sxs-lookup"><span data-stu-id="5dd2e-104">0.9.430 - interface ICoreWebView2DevToolsProtocolEventReceivedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2DevToolsProtocolEventReceivedEventHandler
  : public IUnknown
```

<span data-ttu-id="5dd2e-105">O chamador implementa essa interface para receber eventos do DevToolsProtocolEventReceived da WebView.</span><span class="sxs-lookup"><span data-stu-id="5dd2e-105">The caller implements this interface to receive DevToolsProtocolEventReceived events from the WebView.</span></span>

## <span data-ttu-id="5dd2e-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="5dd2e-106">Summary</span></span>

 <span data-ttu-id="5dd2e-107">Parte</span><span class="sxs-lookup"><span data-stu-id="5dd2e-107">Members</span></span>                        | <span data-ttu-id="5dd2e-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="5dd2e-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="5dd2e-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="5dd2e-109">Invoke</span></span>](#invoke) | <span data-ttu-id="5dd2e-110">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="5dd2e-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="5dd2e-111">Parte</span><span class="sxs-lookup"><span data-stu-id="5dd2e-111">Members</span></span>

#### <span data-ttu-id="5dd2e-112">Invocar</span><span class="sxs-lookup"><span data-stu-id="5dd2e-112">Invoke</span></span> 

<span data-ttu-id="5dd2e-113">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="5dd2e-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="5dd2e-114">Public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* Sender,[ICoreWebView2DevToolsProtocolEventReceivedEventArgs](ICoreWebView2DevToolsProtocolEventReceivedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="5dd2e-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* sender,[ICoreWebView2DevToolsProtocolEventReceivedEventArgs](ICoreWebView2DevToolsProtocolEventReceivedEventArgs.md) \* args)</span></span>

