---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2CapturePreviewCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: 321aff5097783391e4596c22dbd5cb906e45dace
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10881155"
---
# <span data-ttu-id="8ef54-104">0.9.430-ICoreWebView2CapturePreviewCompletedHandler de interface</span><span class="sxs-lookup"><span data-stu-id="8ef54-104">0.9.430 - interface ICoreWebView2CapturePreviewCompletedHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="8ef54-105">Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="8ef54-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="8ef54-106">Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.</span><span class="sxs-lookup"><span data-stu-id="8ef54-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2CapturePreviewCompletedHandler
  : public IUnknown
```

<span data-ttu-id="8ef54-107">O chamador implementa esse método para receber o resultado do método CapturePreview.</span><span class="sxs-lookup"><span data-stu-id="8ef54-107">The caller implements this method to receive the result of the CapturePreview method.</span></span>

## <span data-ttu-id="8ef54-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="8ef54-108">Summary</span></span>

 <span data-ttu-id="8ef54-109">Parte</span><span class="sxs-lookup"><span data-stu-id="8ef54-109">Members</span></span>                        | <span data-ttu-id="8ef54-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="8ef54-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="8ef54-111">Invocar</span><span class="sxs-lookup"><span data-stu-id="8ef54-111">Invoke</span></span>](#invoke) | <span data-ttu-id="8ef54-112">Chamado para fornecer o implementador com o status de conclusão da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="8ef54-112">Called to provide the implementer with the completion status of the corresponding asynchronous method call.</span></span>

<span data-ttu-id="8ef54-113">O resultado é gravado no fluxo fornecido na chamada do método CapturePreview.</span><span class="sxs-lookup"><span data-stu-id="8ef54-113">The result is written to the stream provided in the CapturePreview method call.</span></span>

## <span data-ttu-id="8ef54-114">Parte</span><span class="sxs-lookup"><span data-stu-id="8ef54-114">Members</span></span>

#### <span data-ttu-id="8ef54-115">Invocar</span><span class="sxs-lookup"><span data-stu-id="8ef54-115">Invoke</span></span> 

<span data-ttu-id="8ef54-116">Chamado para fornecer o implementador com o status de conclusão da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="8ef54-116">Called to provide the implementer with the completion status of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="8ef54-117">[chamada](#invoke)a Public HRESULT (resultado HRESULT)</span><span class="sxs-lookup"><span data-stu-id="8ef54-117">public HRESULT [Invoke](#invoke)(HRESULT result)</span></span>

