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
ms.openlocfilehash: 45f1cac30841498f14050c780be83a4898e52408
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652617"
---
# <span data-ttu-id="57ff8-104">interface ICoreWebView2DevToolsProtocolEventReceivedEventHandler</span><span class="sxs-lookup"><span data-stu-id="57ff8-104">interface ICoreWebView2DevToolsProtocolEventReceivedEventHandler</span></span> 

```
interface ICoreWebView2DevToolsProtocolEventReceivedEventHandler
  : public IUnknown
```

<span data-ttu-id="57ff8-105">O chamador implementa essa interface para receber eventos do DevToolsProtocolEventReceived da WebView.</span><span class="sxs-lookup"><span data-stu-id="57ff8-105">The caller implements this interface to receive DevToolsProtocolEventReceived events from the WebView.</span></span>

## <span data-ttu-id="57ff8-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="57ff8-106">Summary</span></span>

 <span data-ttu-id="57ff8-107">Parte</span><span class="sxs-lookup"><span data-stu-id="57ff8-107">Members</span></span>                        | <span data-ttu-id="57ff8-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="57ff8-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="57ff8-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="57ff8-109">Invoke</span></span>](#invoke) | <span data-ttu-id="57ff8-110">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="57ff8-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="57ff8-111">Parte</span><span class="sxs-lookup"><span data-stu-id="57ff8-111">Members</span></span>

#### <span data-ttu-id="57ff8-112">Invocar</span><span class="sxs-lookup"><span data-stu-id="57ff8-112">Invoke</span></span> 

<span data-ttu-id="57ff8-113">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="57ff8-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="57ff8-114">Public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* Sender, [ICoreWebView2DevToolsProtocolEventReceivedEventArgs](icorewebview2devtoolsprotocoleventreceivedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="57ff8-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2DevToolsProtocolEventReceivedEventArgs](icorewebview2devtoolsprotocoleventreceivedeventargs.md) \* args)</span></span>

