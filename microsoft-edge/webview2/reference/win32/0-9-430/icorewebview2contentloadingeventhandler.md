---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2ContentLoadingEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: 7f227e3b2c45b1088b1ac678477cf1dac5ffed5f
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10881127"
---
# <span data-ttu-id="a8f2d-104">0.9.430-ICoreWebView2ContentLoadingEventHandler de interface</span><span class="sxs-lookup"><span data-stu-id="a8f2d-104">0.9.430 - interface ICoreWebView2ContentLoadingEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="a8f2d-105">Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="a8f2d-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="a8f2d-106">Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.</span><span class="sxs-lookup"><span data-stu-id="a8f2d-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2ContentLoadingEventHandler
  : public IUnknown
```

<span data-ttu-id="a8f2d-107">O chamador implementa essa interface para receber o evento ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="a8f2d-107">The caller implements this interface to receive the ContentLoading event.</span></span>

## <span data-ttu-id="a8f2d-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="a8f2d-108">Summary</span></span>

 <span data-ttu-id="a8f2d-109">Parte</span><span class="sxs-lookup"><span data-stu-id="a8f2d-109">Members</span></span>                        | <span data-ttu-id="a8f2d-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="a8f2d-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="a8f2d-111">Invocar</span><span class="sxs-lookup"><span data-stu-id="a8f2d-111">Invoke</span></span>](#invoke) | <span data-ttu-id="a8f2d-112">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="a8f2d-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="a8f2d-113">Parte</span><span class="sxs-lookup"><span data-stu-id="a8f2d-113">Members</span></span>

#### <span data-ttu-id="a8f2d-114">Invocar</span><span class="sxs-lookup"><span data-stu-id="a8f2d-114">Invoke</span></span> 

<span data-ttu-id="a8f2d-115">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="a8f2d-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="a8f2d-116">Public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* WebView,[ICoreWebView2ContentLoadingEventArgs](ICoreWebView2ContentLoadingEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="a8f2d-116">public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* webview,[ICoreWebView2ContentLoadingEventArgs](ICoreWebView2ContentLoadingEventArgs.md) \* args)</span></span>

