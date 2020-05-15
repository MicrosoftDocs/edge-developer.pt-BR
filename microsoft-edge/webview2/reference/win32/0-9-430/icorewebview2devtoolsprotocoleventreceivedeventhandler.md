---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: Microsoft Edge WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/26/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: b786bae624b5f0649ec443e93f741975d672d0e0
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652508"
---
# <span data-ttu-id="d4884-104">interface ICoreWebView2DevToolsProtocolEventReceivedEventHandler</span><span class="sxs-lookup"><span data-stu-id="d4884-104">interface ICoreWebView2DevToolsProtocolEventReceivedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="d4884-105">Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="d4884-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="d4884-106">Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.</span><span class="sxs-lookup"><span data-stu-id="d4884-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2DevToolsProtocolEventReceivedEventHandler
  : public IUnknown
```

<span data-ttu-id="d4884-107">O chamador implementa essa interface para receber eventos do DevToolsProtocolEventReceived da WebView.</span><span class="sxs-lookup"><span data-stu-id="d4884-107">The caller implements this interface to receive DevToolsProtocolEventReceived events from the WebView.</span></span>

## <span data-ttu-id="d4884-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="d4884-108">Summary</span></span>

 <span data-ttu-id="d4884-109">Parte</span><span class="sxs-lookup"><span data-stu-id="d4884-109">Members</span></span>                        | <span data-ttu-id="d4884-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="d4884-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="d4884-111">Invocar</span><span class="sxs-lookup"><span data-stu-id="d4884-111">Invoke</span></span>](#invoke) | <span data-ttu-id="d4884-112">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="d4884-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="d4884-113">Parte</span><span class="sxs-lookup"><span data-stu-id="d4884-113">Members</span></span>

#### <span data-ttu-id="d4884-114">Invocar</span><span class="sxs-lookup"><span data-stu-id="d4884-114">Invoke</span></span> 

<span data-ttu-id="d4884-115">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="d4884-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="d4884-116">Public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* Sender,[ICoreWebView2DevToolsProtocolEventReceivedEventArgs](ICoreWebView2DevToolsProtocolEventReceivedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="d4884-116">public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* sender,[ICoreWebView2DevToolsProtocolEventReceivedEventArgs](ICoreWebView2DevToolsProtocolEventReceivedEventArgs.md) \* args)</span></span>

