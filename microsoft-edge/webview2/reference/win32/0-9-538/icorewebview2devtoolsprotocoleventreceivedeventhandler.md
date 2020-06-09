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
ms.openlocfilehash: c154b80e29476666bc0b2121b3eba63009946b36
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698290"
---
# <span data-ttu-id="f4b2d-104">interface ICoreWebView2DevToolsProtocolEventReceivedEventHandler</span><span class="sxs-lookup"><span data-stu-id="f4b2d-104">interface ICoreWebView2DevToolsProtocolEventReceivedEventHandler</span></span> 

```
interface ICoreWebView2DevToolsProtocolEventReceivedEventHandler
  : public IUnknown
```

<span data-ttu-id="f4b2d-105">O chamador implementa essa interface para receber eventos do DevToolsProtocolEventReceived da WebView.</span><span class="sxs-lookup"><span data-stu-id="f4b2d-105">The caller implements this interface to receive DevToolsProtocolEventReceived events from the WebView.</span></span>

## <span data-ttu-id="f4b2d-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="f4b2d-106">Summary</span></span>

 <span data-ttu-id="f4b2d-107">Parte</span><span class="sxs-lookup"><span data-stu-id="f4b2d-107">Members</span></span>                        | <span data-ttu-id="f4b2d-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="f4b2d-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="f4b2d-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="f4b2d-109">Invoke</span></span>](#invoke) | <span data-ttu-id="f4b2d-110">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="f4b2d-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="f4b2d-111">Parte</span><span class="sxs-lookup"><span data-stu-id="f4b2d-111">Members</span></span>

#### <span data-ttu-id="f4b2d-112">Invocar</span><span class="sxs-lookup"><span data-stu-id="f4b2d-112">Invoke</span></span> 

<span data-ttu-id="f4b2d-113">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="f4b2d-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="f4b2d-114">Public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* Sender, [ICoreWebView2DevToolsProtocolEventReceivedEventArgs](icorewebview2devtoolsprotocoleventreceivedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="f4b2d-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2DevToolsProtocolEventReceivedEventArgs](icorewebview2devtoolsprotocoleventreceivedeventargs.md) \* args)</span></span>

