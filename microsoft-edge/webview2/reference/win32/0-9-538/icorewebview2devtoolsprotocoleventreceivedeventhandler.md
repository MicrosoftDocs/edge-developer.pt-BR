---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2DevToolsProtocolEventReceivedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2DevToolsProtocolEventReceivedEventHandler
ms.openlocfilehash: 163ab3f16b6d835fc64aef4ea0fdff2883084faa
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010261"
---
# <span data-ttu-id="90c2b-104">0.9.579-ICoreWebView2DevToolsProtocolEventReceivedEventHandler de interface</span><span class="sxs-lookup"><span data-stu-id="90c2b-104">0.9.579 - interface ICoreWebView2DevToolsProtocolEventReceivedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2DevToolsProtocolEventReceivedEventHandler
  : public IUnknown
```

<span data-ttu-id="90c2b-105">O chamador implementa essa interface para receber eventos do DevToolsProtocolEventReceived da WebView.</span><span class="sxs-lookup"><span data-stu-id="90c2b-105">The caller implements this interface to receive DevToolsProtocolEventReceived events from the WebView.</span></span>

## <span data-ttu-id="90c2b-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="90c2b-106">Summary</span></span>

 <span data-ttu-id="90c2b-107">Parte</span><span class="sxs-lookup"><span data-stu-id="90c2b-107">Members</span></span>                        | <span data-ttu-id="90c2b-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="90c2b-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="90c2b-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="90c2b-109">Invoke</span></span>](#invoke) | <span data-ttu-id="90c2b-110">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="90c2b-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="90c2b-111">Parte</span><span class="sxs-lookup"><span data-stu-id="90c2b-111">Members</span></span>

#### <span data-ttu-id="90c2b-112">Invocar</span><span class="sxs-lookup"><span data-stu-id="90c2b-112">Invoke</span></span> 

<span data-ttu-id="90c2b-113">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="90c2b-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="90c2b-114">Public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* Sender, [ICoreWebView2DevToolsProtocolEventReceivedEventArgs](icorewebview2devtoolsprotocoleventreceivedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="90c2b-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2DevToolsProtocolEventReceivedEventArgs](icorewebview2devtoolsprotocoleventreceivedeventargs.md) \* args)</span></span>

