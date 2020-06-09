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
ms.openlocfilehash: a38d451f4ee99e4ab1392f4685a66abf1f274ddb
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698061"
---
# <span data-ttu-id="ca69b-104">interface ICoreWebView2DevToolsProtocolEventReceivedEventHandler</span><span class="sxs-lookup"><span data-stu-id="ca69b-104">interface ICoreWebView2DevToolsProtocolEventReceivedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="ca69b-105">Esta referência pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="ca69b-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="ca69b-106">Consulte a [referência de API WebView2](../../../webview2-api-reference.md) para obter a referência de API mais recente.</span><span class="sxs-lookup"><span data-stu-id="ca69b-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2DevToolsProtocolEventReceivedEventHandler
  : public IUnknown
```

<span data-ttu-id="ca69b-107">O chamador implementa essa interface para receber eventos do DevToolsProtocolEventReceived da WebView.</span><span class="sxs-lookup"><span data-stu-id="ca69b-107">The caller implements this interface to receive DevToolsProtocolEventReceived events from the WebView.</span></span>

## <span data-ttu-id="ca69b-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="ca69b-108">Summary</span></span>

 <span data-ttu-id="ca69b-109">Parte</span><span class="sxs-lookup"><span data-stu-id="ca69b-109">Members</span></span>                        | <span data-ttu-id="ca69b-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="ca69b-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="ca69b-111">Invocar</span><span class="sxs-lookup"><span data-stu-id="ca69b-111">Invoke</span></span>](#invoke) | <span data-ttu-id="ca69b-112">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="ca69b-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="ca69b-113">Parte</span><span class="sxs-lookup"><span data-stu-id="ca69b-113">Members</span></span>

#### <span data-ttu-id="ca69b-114">Invocar</span><span class="sxs-lookup"><span data-stu-id="ca69b-114">Invoke</span></span> 

<span data-ttu-id="ca69b-115">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="ca69b-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="ca69b-116">Public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* Sender, [ICoreWebView2DevToolsProtocolEventReceivedEventArgs](icorewebview2devtoolsprotocoleventreceivedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="ca69b-116">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2DevToolsProtocolEventReceivedEventArgs](icorewebview2devtoolsprotocoleventreceivedeventargs.md) \* args)</span></span>

