---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2SourceChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: 1e3e9d3f661a6e0643d7094c9127fdf33501624a
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880175"
---
# <span data-ttu-id="4591d-104">0.9.430-ICoreWebView2SourceChangedEventHandler de interface</span><span class="sxs-lookup"><span data-stu-id="4591d-104">0.9.430 - interface ICoreWebView2SourceChangedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="4591d-105">Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="4591d-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="4591d-106">Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.</span><span class="sxs-lookup"><span data-stu-id="4591d-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2SourceChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="4591d-107">O chamador implementa essa interface para receber o evento SourceChanged.</span><span class="sxs-lookup"><span data-stu-id="4591d-107">The caller implements this interface to receive the SourceChanged event.</span></span>

## <span data-ttu-id="4591d-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="4591d-108">Summary</span></span>

 <span data-ttu-id="4591d-109">Parte</span><span class="sxs-lookup"><span data-stu-id="4591d-109">Members</span></span>                        | <span data-ttu-id="4591d-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="4591d-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="4591d-111">Invocar</span><span class="sxs-lookup"><span data-stu-id="4591d-111">Invoke</span></span>](#invoke) | <span data-ttu-id="4591d-112">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="4591d-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="4591d-113">Parte</span><span class="sxs-lookup"><span data-stu-id="4591d-113">Members</span></span>

#### <span data-ttu-id="4591d-114">Invocar</span><span class="sxs-lookup"><span data-stu-id="4591d-114">Invoke</span></span> 

<span data-ttu-id="4591d-115">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="4591d-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="4591d-116">Public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* WebView,[ICoreWebView2SourceChangedEventArgs](ICoreWebView2SourceChangedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="4591d-116">public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* webview,[ICoreWebView2SourceChangedEventArgs](ICoreWebView2SourceChangedEventArgs.md) \* args)</span></span>

