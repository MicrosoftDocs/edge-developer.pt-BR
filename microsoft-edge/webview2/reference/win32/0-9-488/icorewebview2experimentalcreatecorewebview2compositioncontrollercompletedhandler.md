---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: f2598d40afc7c7def1c3fec634016f1a64905479
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885664"
---
# <span data-ttu-id="fc981-104">0.9.515-ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler de interface</span><span class="sxs-lookup"><span data-stu-id="fc981-104">0.9.515 - interface ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler</span></span> 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

```
interface ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler
  : public IUnknown
```

<span data-ttu-id="fc981-105">O chamador implementa essa interface para receber a CoreWebView2Controller criada via CreateCoreWebView2CompositionController.</span><span class="sxs-lookup"><span data-stu-id="fc981-105">The caller implements this interface to receive the CoreWebView2Controller created via CreateCoreWebView2CompositionController.</span></span>

## <span data-ttu-id="fc981-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="fc981-106">Summary</span></span>

 <span data-ttu-id="fc981-107">Parte</span><span class="sxs-lookup"><span data-stu-id="fc981-107">Members</span></span>                        | <span data-ttu-id="fc981-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="fc981-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="fc981-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="fc981-109">Invoke</span></span>](#invoke) | <span data-ttu-id="fc981-110">Chamado para fornecer o implementador com o status de conclusão e o resultado da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="fc981-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="fc981-111">Parte</span><span class="sxs-lookup"><span data-stu-id="fc981-111">Members</span></span>

#### <span data-ttu-id="fc981-112">Invocar</span><span class="sxs-lookup"><span data-stu-id="fc981-112">Invoke</span></span> 

<span data-ttu-id="fc981-113">Chamado para fornecer o implementador com o status de conclusão e o resultado da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="fc981-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="fc981-114">[chamada](#invoke)a Public HRESULT (resultado HRESULT, [ICoreWebView2ExperimentalCompositionController](icorewebview2experimentalcompositioncontroller.md) \* WebView)</span><span class="sxs-lookup"><span data-stu-id="fc981-114">public HRESULT [Invoke](#invoke)(HRESULT result, [ICoreWebView2ExperimentalCompositionController](icorewebview2experimentalcompositioncontroller.md) \* webView)</span></span>

